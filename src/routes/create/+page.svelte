<script>
    import { goto } from '$app/navigation';
    import {base} from '$app/paths';
    import { browser } from "$app/environment";
    import { onMount } from 'svelte';
    
    let projectIDs = {}
    onMount(()=>{
        if (!browser) return

        let raw = localStorage.getItem("projectIDs")
        if (raw){
            projectIDs = JSON.parse(raw)
        }
    })

    function get_new_id(){
        let id = "p"+45678
        while (Object.hasOwn(projectIDs, id)){
            id = "p"+Math.floor(Math.random()*999999)
        }
        return id
    }

    function newGame() {
        let id = get_new_id()
        projectIDs[id] = {}
        localStorage.setItem("projectIDs", JSON.stringify(projectIDs))
        localStorage.setItem(
            `project_${id}`,
            JSON.stringify({})
        );

        goto(base + '/create/' + id);
    }

</script>

<main>
    <button onclick={newGame}>Create new game</button>
</main>

<style>

main{
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>
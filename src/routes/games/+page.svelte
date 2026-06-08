<script>
    import { defaultProjects } from '$lib/defaults'
    import { goto } from '$app/navigation';
    import {base} from '$app/paths';
    import { browser } from "$app/environment";
    import { onMount } from 'svelte';
    
    let games = $state({})
    onMount(()=>{
        if (!browser) return

        let raw = localStorage.getItem("projectIDs")
        if (raw){
            games = JSON.parse(raw)
        }
    })

</script>



<main>
    <h1>Games</h1>
    <h2>Default games</h2>
    <div class="game_container">
        {#each Object.entries(defaultProjects) as [id, data]}
            <a href={base+'/create/'+id}>{data.name}</a>
        {/each}

    </div>
    <h2>My games</h2>
    <div class="game_container">
        {#if browser}
            {#each Object.entries(games) as [id, data]}
                {@const game = JSON.parse(localStorage.getItem("project_"+id))}
                {#if game}
                    <a href={base+'/create/'+id}>
                        <p>{game.name}</p>
                    </a>
                {/if}        
            {/each}
        {/if}

    </div>
</main>



<style>

main{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: rgb(179, 179, 179);
    width: 50vw;
    height: 80vh;
    justify-self: center;
    margin: 10vh;
    overflow-y: auto;
    border-radius: 30px;
}
.game_container{
    display: flex;
    flex-wrap: wrap;
    width: 90%;
}
a{
    background-color: #505050;
    width: 100px;
    height: 100px;
    margin: 10px;
    border-style: solid;
    border-width: 10px;
    border-radius: 20px;
    border-color: black;
    color: white;
    display: flex;
    justify-content: center;
    align-items: end;
    padding: 10px;
    text-decoration: none;
}
a:hover{
    transform: scale(1.1);
}

</style>
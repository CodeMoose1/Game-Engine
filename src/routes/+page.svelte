<script>
import { base } from '$app/paths';
</script>

<main>
    <h1>Welcome to BenEngine2.0</h1>

    <div class="button_container">
        <a href="{base}/games">My games</a>
        <a href="{base}/create">Create new</a>
    </div>
</main>

<style>

main{
    display:flex;
    flex-direction: column;

    height:100%;
    
    align-items: center;
    justify-content: center;
    
}
.button_container{
    justify-content: space-between;
}
a{  
    color: black;
    text-decoration: none;
    background-color: dimgrey;
    padding: 10px;

    border-style: solid;
    border-width: 4px;
    border-radius: 10px;

    transition: all 0.2s ease-out;
}
a:hover{
    background-color: gray;
    padding-left: 30px;
    padding-right: 30px;
    
}
    
</style>
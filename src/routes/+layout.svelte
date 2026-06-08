<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();

</script>



<svelte:head>
	<link rel="icon" href={favicon} />
	<link
            rel="stylesheet"
            href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
    />
</svelte:head>

<style>
:global(body), :global(html){
	margin: 0%;
	padding: 0%;
	height: 100vh;
	width: 100vw;
	overflow: hidden;
}
</style>

{@render children()}

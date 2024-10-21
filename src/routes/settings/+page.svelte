

<script lang="ts">
    import Blog from "../blog/+page.svelte"
    let name:string = "Winthedev";
</script>

<svelte:head>
	<title>Settings</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
    <h1>Settings</h1>
    <h2>{name}</h2>
    <h3>Blog below</h3>
    <Blog/>
</section>
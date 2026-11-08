<script>
	import favicon from '#lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>CineVault</title>
</svelte:head>

<nav class="navbar navbar-expand bg-dark border-bottom sticky-top">
	<div class="container-fluid">
		<a class="navbar-brand fw-bold" href="/">🎬 CineVault</a>
		<div class="navbar-nav">
			<a class="nav-link" href="/movies">Movies</a>
		</div>
	</div>
</nav>

{@render children()}

<style>
	:global(body) {
		background-color: #000;
	}
</style>
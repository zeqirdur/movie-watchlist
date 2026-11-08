<script>
	import MovieCard from "#lib/components/MovieCard.svelte";

	let { data } = $props();
</script>

<div class="container">
	<div class="py-5">
		<h1 class="display-4 fw-bold">🎬 Welcome to CineVault</h1>
		<a href="/movies" class="btn btn-warning btn-lg mt-2">Alle Filme ansehen</a>
	</div>

	<h2 class="h4 mb-3">Neu bei CineVault</h2>
	<div class="row row-cols-2 row-cols-md-4 g-3 mb-5">
		{#each data.movies.slice(0, 4) as movie}
			<div class="col">
				<MovieCard movie={movie} />
			</div>
		{/each}
	</div>
</div>
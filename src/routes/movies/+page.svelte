<script>
	import MovieCard from "#lib/components/MovieCard.svelte";

	let { data } = $props();
</script>

<div class="container">
	<div class="d-flex justify-content-between align-items-center mt-4">
		<h1 class="h3">Alle Filme</h1>
		<a href="/movies/create" class="btn btn-warning">+ Film hinzufügen</a>
	</div>
	<p class="fst-italic text-secondary">Daten und Bilder generiert mit KI</p>

	<div class="row row-cols-2 row-cols-md-3 row-cols-lg-4 g-3 mb-4">
		{#each data.movies as movie}
			<div class="col">
				<MovieCard movie={movie} />
			</div>
		{/each}
	</div>
</div>
<script>
	let { data } = $props();
</script>

<div class="container py-4">
	<a href="/movies" class="link-light">← Zurück zu allen Filmen</a>

	<div class="row mt-3 g-4">
		<div class="col-md-4">
			<img src={data.movie.poster} class="img-fluid rounded" alt={"Poster von " + data.movie.title} />
		</div>

		<div class="col-md-8">
			<h1>{data.movie.title}</h1>
			<p class="mb-1"><b>Jahr:</b> {data.movie.year}</p>
			<p><b>Dauer:</b> {data.movie.length}</p>

			<h2 class="h5 mt-4">Schauspieler</h2>
			<ul>
				{#each data.movie.actors as actor}
					<li>{actor}</li>
				{/each}
			</ul>
		</div>
	</div>
</div>
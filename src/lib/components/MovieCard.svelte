<script>
	let { movie } = $props();
</script>

<div class="card h-100">
	<img src={movie.poster} class="card-img-top" alt={"Poster von " + movie.title} />
	<div class="card-body">
		<h6 class="card-title fw-bold mb-1">
			<a href={"/movies/" + movie._id} class="link-light">{movie.title}</a>
		</h6>
		<p class="card-text mb-0">Jahr: {movie.year}</p>
		<p class="card-text">Dauer: {movie.length}</p>
	</div>
</div>
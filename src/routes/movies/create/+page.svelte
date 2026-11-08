<script>
	let { form } = $props();
</script>

<div class="container py-4" style="max-width: 600px;">
	<a href="/movies" class="link-light">← Zurück zu allen Filmen</a>
	<h1 class="h3 mt-3">Neuen Film erfassen</h1>

	<form method="POST" action="?/create">
		<div class="mb-3">
			<label for="title" class="form-label">Titel</label>
			<input id="title" name="title" class="form-control" type="text" required />
		</div>
		<div class="mb-3">
			<label for="year" class="form-label">Jahr</label>
			<input id="year" name="year" class="form-control" type="number" required />
		</div>
		<div class="mb-3">
			<label for="length" class="form-label">Dauer</label>
			<input id="length" name="length" class="form-control" type="text" placeholder="z.B. 114 Minuten" required />
		</div>
		<button type="submit" class="btn btn-warning">Film hinzufügen</button>
	</form>

	{#if form?.success}
		<div class="alert alert-success mt-3">Film wurde hinzugefügt!</div>
	{/if}
</div>
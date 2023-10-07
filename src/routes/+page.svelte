<script>
	import { CldImage } from 'svelte-cloudinary';

	const src = 'orange-cat';
	const alt = 'An orange cat with its head leaning to one side, looking quizzically at the camera';
</script>

<div class="card">
	<CldImage height={840} width={700} {src} {alt} class="big-image" />

	<div class="content">
		<div class="title">
			<CldImage height={200} width={200} {src} {alt} class="small-image" crop="thumb" />
			<h1>Sunny</h1>
		</div>
		<p>
			Meet our charming orange tabby cat! This delightful feline, with its vibrant orange coat and
			captivating eyes, is sure to steal your heart. Known for its playful and affectionate nature,
			this cat is the perfect companion for both families and individuals. Whether it's curling up
			on your lap for a cozy evening or entertaining you with its playful antics, this cat is full
			of personality. We've affectionately nicknamed them "Sunny," but you can choose from a range
			of names like "Amber," "Marmalade," or "Leo" to suit their sunny disposition. Don't miss out
			on the chance to bring a ray of sunshine into your life – adopt this orange beauty today!
		</p>
	</div>
</div>

<style>
	.card {
		font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans,
			sans-serif;
		display: grid;
		grid-template-columns: 1fr;
		border-radius: 1rem;
		border: 1px solid lightgrey;
		overflow: hidden;
		max-width: 800px;
		margin: 0 auto;
		align-items: center;
	}

	.content {
		padding: 1rem;
		line-height: 1.4;
	}

	.card :global(.big-image) {
		display: none;
	}

	.card :global(.small-image) {
		border-radius: 100%;
		flex-basis: 125px;
	}

	.title {
		display: flex;
		gap: 1rem;
		align-items: center;
	}

	@media (min-width: 600px) {
		.card {
			grid-template-columns: 300px 1fr;
		}

		.card :global(.big-image) {
			display: block;
			align-self: stretch;
		}

		.card :global(.small-image) {
			display: none;
		}
	}
</style>

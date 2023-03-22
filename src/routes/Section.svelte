<script>
	import { browser } from '$app/environment';
	import { onMount, onDestroy } from 'svelte';

	export let props = { sectionId: '', title: '', description: '', image: '', color: '' };
	const { sectionId, title, description, image, color = '#ffffff' } = props;
	let injected = false;

	if (browser) {
	}
</script>

<div class="main-sections">
	<div class="text-section">
		<h1>{title}</h1>
		<span>{description}</span>
	</div>
</div>

<style>
	.text-section.active {
		opacity: 0;
	}
	.main-sections {
		height: 24rem;
		display: flex;
		flex-direction: column;
		align-items: start;
		width: 100%;
	}
	.text-section {
		width: 120px;
		padding: 4rem;
		opacity: 1;
		background-color: red;
		transition: all 2s ease-in-out;
	}
</style>

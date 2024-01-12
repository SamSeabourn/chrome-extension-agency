<script lang="ts">
	import { base } from '$app/paths';
</script>

<section id="hero">
	<slot />
</section>
<div class="repeating-pattern" style="background-image: url({base + '/repeater.webp'})" />
<div class="gradient-overlay" />

<style>
	section {
		width: 100%;
		height: 74vh;
		padding-top: 5rem;
		background-color: #f2f3f6;
	}

	.repeating-pattern {
		background-repeat: repeat;
		position: absolute;
		width: 1000%;
		height: 100%;
		top: 0;
		background-size: 40rem;
	}

	.gradient-overlay {
		position: absolute;
		width: 130rem;
		height: 100%;
		top: 0;
		background:linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 100%);

	}
</style>

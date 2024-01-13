<script lang="ts">
	import { base } from '$app/paths';
	import { onMount } from 'svelte';

	let currentScroll = 0;

	onMount(() => {
		document.addEventListener('scroll', () => {
			currentScroll =
				window.pageYOffset !== undefined
					? window.pageYOffset
					: (document.documentElement || document.body.parentNode || document.body)
							.scrollTop;
		});
	});
</script>

<div class="wrapper">
	<div class="large-cog-wrapper">
		<div style="transform: rotate({currentScroll / 30}deg);">
			<img src="{base}/big-cog.svg" alt="Large cog" id="largeCog" />
		</div>
	</div>
	<div class="medium-cog-wrapper">
		<div style="transform: rotate(-{currentScroll / 20}deg);">
			<img src="{base}/medium-cog.svg" alt="Medium cog" id="mediumCog" />
		</div>
	</div>
	<div class="small-cog-wrapper">
		<div style="transform: rotate({currentScroll / 10}deg);">
			<img src="{base}/small-cog.svg" alt="Small cog" id="smallCog" />
		</div>
	</div>
</div>

<style>
	img {
		filter: drop-shadow(0px 0px 8px rgba(0, 0, 0, 0.2));
	}

	@keyframes rotate {
		from {
			transform: rotate(0deg);
		}
		to {
			transform: rotate(360deg);
		}
	}
	.wrapper {
		position: fixed;
		top: 0px;
		scale: 0.9;
		right: 0rem;
		z-index: 10;
	}

	#largeCog {
		width: 18rem;
	}

	.large-cog-wrapper {
		position: absolute;
		right: -3rem;
		top: -5rem;
		z-index: 10;
	}

	#mediumCog {
		width: 12rem;
	}

	.medium-cog-wrapper {
		position: absolute;
		right: 7rem;
		top: 12.5rem;
		z-index: 10;
	}

	#smallCog {
		width: 7rem;
	}

	.small-cog-wrapper {
		position: absolute;
		right: 2rem;
		top: 22rem;
		z-index: 10;
	}
</style>

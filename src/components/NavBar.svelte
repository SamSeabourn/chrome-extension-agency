<script lang="ts">
	import { base } from '$app/paths';
	export let title: string;
</script>

<nav>
	<a href="{base}/" aria-label="Home page">
		<div class="the-wrapper"><h3>THE</h3></div>
		<h1>{title}</h1>
	</a>
</nav>

<style>
	@font-face {
		font-family: 'Bungee-Regular';
		src: url('$lib/assets/fonts/Bungee-Regular.ttf');
		font-display: swap;
	}
	nav {
		height: 6rem;
		width: 100%;
		box-shadow: 0px 4px 24px 0px rgba(0, 0, 0, 0.15);
		display: flex;
		align-items: center;
		position: fixed;
		background-color: #fdfdfd;
		z-index: 30;
	}
	h1 {
		font-family: 'Bungee-Regular', sans-serif;
		font-size: 2.7rem;
		font-weight: 900;
		letter-spacing: -0.03rem;
	}

	.the-wrapper {
		margin-left: 3rem;
		display: flex;
		align-items: center;
		color: #05d2d9;
	}

	h3 {
		transform: rotate(-90deg) translateY(0.5rem);
	}

	a {
		font-family: 'Bungee-Regular', sans-serif;
		display: flex;
		color: #170d1e;
		text-decoration: none;
	}

	a:hover,
	a:visited {
		color: #170d1e;
		text-decoration: none;
	}
</style>

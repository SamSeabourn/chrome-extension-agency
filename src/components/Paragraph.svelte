<p>
	<slot />
</p>

<style>
	@font-face {
		font-family: 'Inter';
		src: url('$lib/assets/fonts/Inter-Regular.ttf');
		font-display: swap;
	}
	p {
		font-family: 'Inter', sans-serif;
		width: 35rem;
		color: #170d1e;
		line-height: 1.3rem;
		font-size: 1.25rem;
	}

	@media (max-width: 1640px) {
		p {
			width: 32.75rem;
		}
	}
</style>

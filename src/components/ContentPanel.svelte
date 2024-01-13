<section>
	<slot />
</section>

<style>
	section {
		background-color: #fdfdfd;
		width: 100%;
		clip-path: polygon(21rem 0, 100% 9rem, 100% 100%, 0 100%, 0 4rem);
		padding-top: 4rem;
		z-index: 1;
	}

	@media (max-width: 1080px) {
		section {
			z-index: 10;
			position: absolute;
		}
	}
</style>

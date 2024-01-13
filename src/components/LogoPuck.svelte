<script lang="ts">
	export let imageSource: string;
	export let imageAlt: string;
</script>

<div>
	<img src={imageSource} alt={imageAlt} />
</div>

<style>
	div {
		height: 5.5rem;
		display: flex;
		width: 5.5rem;
		border-radius: 5.5rem;
		background-color: #fff;
		filter: drop-shadow(0px 0px 6px rgba(0, 0, 0, 0.3));
		justify-content: center;
		align-items: center;
		margin-right: 1rem;
		margin-top: 1rem;
	}

	img {
		width: 3rem;
	}
</style>

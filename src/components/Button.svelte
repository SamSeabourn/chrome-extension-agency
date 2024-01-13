<script lang="ts">
	export let btnFunc: () => object;
</script>

<button on:click={() => btnFunc()}>
	<slot />
</button>

<style>
	button {
		width: 13rem;
		height: 3.5rem;
		background-color: #05d2d9;
		border: none;
		font-size: 1rem;
		border-radius: 2rem;
	}

	button:hover {
		background-color: transparent;
		border: 3px solid #05d2d9;
		color: white;
		font-size: 1rem;
		border-radius: 2rem;
		cursor: pointer;
	}
</style>

<script lang="ts">
	import { generateGUID } from '../helpers/generate-guid';
	import FadeInOnScroll from './FadeInOnScroll.svelte';
	import ImageCircle from './ImageCircle.svelte';

	import Paragraph from './Paragraph.svelte';
	export let userName: string;
	export let imageSource: string;
</script>

<FadeInOnScroll id={generateGUID()}>
	<div class="testimonal">
		<ImageCircle {imageSource} imageAlt={`Image of user ${userName}`} />
		<div class="writeup">
			<Paragraph>
				<slot />
				<br />
				<span>{userName}</span>
			</Paragraph>
		</div>
	</div>
</FadeInOnScroll>

<style>
	span {
		color: #05d2d9;
	}

	.testimonal {
		align-items: center;
		display: inline-flex;
		margin-bottom: 3.5rem;
		margin-top: 1rem;
	}

	.writeup {
		margin-left: 1.5rem;
	}

	@media (max-width: 500px) {
		.testimonal {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
		}

		.writeup {
			margin-top: 2rem;
			margin-left: 0rem;
		}
	}
</style>

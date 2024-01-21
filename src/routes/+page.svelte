<script>
	import { base } from '$app/paths';
	import AirGap from '../components/AirGap.svelte';
	import CTA from '../components/CTA.svelte';
	import Cogs from '../components/Cogs.svelte';
	import ContentPadding from '../components/ContentPadding.svelte';
	import ContentPanel from '../components/ContentPanel.svelte';
	import FadeInOnScroll from '../components/FadeInOnScroll.svelte';
	import Footer from '../components/Footer.svelte';
	import HeroPanel from '../components/HeroPanel.svelte';
	import HeroText from '../components/HeroText.svelte';
	import LogoPuck from '../components/LogoPuck.svelte';
	import NavBar from '../components/NavBar.svelte';
	import Paragraph from '../components/Paragraph.svelte';
	import Title from '../components/Title.svelte';
</script>

<NavBar title={'Chrome Extension Agency'} />
<Cogs />
<HeroPanel>
	<HeroText />
</HeroPanel>
<ContentPanel>
	<ContentPadding>
		<Title label="Extend the web">Extend the web</Title>
		<Paragraph>
			We specialize in crafting custom extensions for Twitch, Chrome, and Firefox. We empower
			businesses and individual creators to elevate their online presence through bespoke
			plugins. Whether you're looking to enhance user engagement, integrate an existing
			product, or unlock new capabilities, our team of expert developers can bring your vision
			to life. Partner with us to transform your ideas into reality, and extend your reach in
			the ever-evolving web landscape
		</Paragraph>
		<div style="display:flex">
			<LogoPuck imageSource="{base}/chrome-logo.svg" imageAlt="Google Chrome" />
			<LogoPuck imageSource="{base}/firefox-logo.svg" imageAlt="Firefox Browser" />
			<LogoPuck imageSource="{base}/twitch-logo.svg" imageAlt="Twitch" />
			<LogoPuck imageSource="{base}/chatgpt-logo.svg" imageAlt="Chat GPT" />
		</div>
		<AirGap />
		<FadeInOnScroll id={'youDecide'}>
			<Title label="You decide">You Decide</Title>
			<Paragraph>
				We offer the flexibility to choose your preferred technology, ensuring our solutions
				align perfectly with your existing codebase. Our team is skilled in a range of
				technologies, ready to adapt to your specific needs for seamless integration
			</Paragraph>
			<div style="display:flex">
				<LogoPuck imageSource="{base}/react-logo.svg" imageAlt="ReactJS" />
				<LogoPuck imageSource="{base}/svelte-logo.svg" imageAlt="SvelteKit" />
				<LogoPuck imageSource="{base}/angular-logo.svg" imageAlt="AngularJS" />
				<LogoPuck imageSource="{base}/vue-logo.svg" imageAlt="VueJS" />
			</div>
			<div style="display:flex;margin-left: 3rem">
				<LogoPuck imageSource="{base}/js-logo.svg" imageAlt="Javascript" />
				<LogoPuck imageSource="{base}/ts-logo.svg" imageAlt="Typescript" />
				<LogoPuck imageSource="{base}/mui-logo.svg" imageAlt="Material UI" />
				<LogoPuck imageSource="{base}/tailwind-logo.svg" imageAlt="Tailwind" />
			</div>
		</FadeInOnScroll>
		<AirGap />
		<CTA href={'chromeextension.agency'}>Lets build something together</CTA>
		<AirGap />
	</ContentPadding>
	<Footer />
</ContentPanel>

<script>
	import Hero from "./components/Hero.svelte"
	import Counter from "./components/Counter.svelte"
	import FeatureDescription from "./components/FeatureDescription.svelte"
	import Footer from "./components/Footer.svelte"
</script>

<div class="lp">
	<Hero />
	<Counter count="1" />
	<FeatureDescription />
	<Counter count="2" />
	<Footer />
</div>

<style>
	.lp {
		overflow-x: hidden;
	}
</style>
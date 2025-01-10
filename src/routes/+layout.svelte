<script>
	import '../app.css';
	import Headerfinal from '../components/header/headerfinal.svelte';
	import Languagedropdown from '../components/header/languagedropdown.svelte';

	import { addMessages, init, getLocaleFromNavigator } from 'svelte-i18n';
	import nl from '../locale/nl.json';
	import en from '../locale/en.json';
	
	addMessages('en', en);
	addMessages('nl', nl);

	init({
		fallbackLocale: 'en',
		initialLocale: getLocaleFromNavigator()
	});

	let { children } = $props();
</script>

<Languagedropdown />

<div class="container h-full mx-auto px-8 pb-8">
	<Headerfinal />

	<div class="mb-6"></div>
	<!-- Spacing -->

	{@render children()}
</div>

<style>
	.container {
		max-width: 1216px;
	}
</style>

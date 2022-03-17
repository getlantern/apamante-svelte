<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<div class="content">
	<h1>About Apamante</h1>

	<p>
		Founded in 2017, Apamante is a Panamanian foundation that is dedicated to the eradication of financial 
		censorship around the world. Financial censorship causes countless problems and takes many forms, 
		whether it is outrageously high fees charged for cross border payments and remittances, or whether it is 
		limits on moving money in and out of countries. It is hugely damaging to the fabric of our society, and 
		Apamante works to make it a thing of the past through the use of virtual currencies within regulatory limits.
	</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>

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
	<h1>About this app</h1>

	<p>
		<a href="https://kit.svelte.dev">SvelteKit</a> app を使用したサンプルです。
		シンプルなカウンター、TODOがあります:
	</p>

	<!-- TODO lose the @next! 
	<pre>npm init svelte@next</pre>
	-->

	<p>
		さてここでは、vercelを用いたビルドについて記します。
		Githubにプロジェクトを作りpushしたらvercelが自動でビルド、デプロイを行います
	</p>

	<p>
		The <a href="/todos">TODOs</a> page illustrates SvelteKit's data loading and form handling. Try using
		it with JavaScript disabled!
	</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>

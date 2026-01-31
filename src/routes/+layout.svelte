<script>
	import './layout.css';
	import { page } from '$app/stores';
	import favicon from '$lib/assets/favicon.svg';
	import icon from '$lib/assets/icon.png';
	import logo from '$lib/assets/logo-text.png';
	import { AppBar } from '@skeletonlabs/skeleton-svelte';

	let { children } = $props();
	
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

{#if $page.url.pathname !== "/"}	
<AppBar class="preset-glass-surface p-0">
	<AppBar.Toolbar class="grid-cols-[1fr_2fr_1fr]">
		<AppBar.Lead>
			<a href="/"><img src={icon} alt="Splash Page Link Button" class="nav-img opacity-50" /></a>
		</AppBar.Lead>
		<AppBar.Headline class="flex justify-center">
			<a href="/"><img src={logo} alt="Splash Page Link Button" class="nav-img" /></a>
		</AppBar.Headline>
		<AppBar.Trail class="justify-around">
			<a href="/music" class="nav-link hover:preset-tonal">Music</a>
			<a href="/videos" class="nav-link hover:preset-tonal">Videos</a>
			<a href="/about" class="nav-link hover:preset-tonal">About</a>
			<a href="/lessons" class="nav-link hover:preset-tonal">Lessons</a>
		</AppBar.Trail>
	</AppBar.Toolbar>
</AppBar>
{/if}

<main>
	{@render children()}
</main>

<style>
	.nav-img {
		height: 60px;
	}
</style>

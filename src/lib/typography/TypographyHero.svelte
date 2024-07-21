<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HeadingTags, Size } from '../index.jss';

	type TypographyHeroProps = {
		children: Snippet;
		tag: HeadingTags;
		size: Size;
	};

	let { children, tag = 'h1', size = 'md' }: TypographyHeroProps = $props();

	let typographyClasses = `typography-hero-${size}`;
</script>

<svelte:element this={tag} class={typographyClasses}>
	{#if children}
		{@render children()}
	{/if}
</svelte:element>

<style>
	.typography-hero-sm {
		font-family: var(--typography-typeface-hero-sm-font-family);
		font-weight: var(--typography-typeface-hero-sm-font-weight);
		font-size: var(--typography-typescale-hero-sm-font-size);
		letter-spacing: var(--typography-typescale-hero-sm-letter-spacing);
		line-height: var(--typography-typescale-hero-sm-line-height);
	}
	.typography-hero-md {
		font-family: var(--typography-typeface-hero-md-font-family);
		font-weight: var(--typography-typeface-hero-md-font-weight);
		font-size: var(--typography-typescale-hero-md-font-size);
		letter-spacing: var(--typography-typescale-hero-md-letter-spacing);
		line-height: var(--typography-typescale-hero-md-line-height);
	}
	.typography-hero-lg {
		font-family: var(--typography-typeface-hero-lg-font-family);
		font-weight: var(--typography-typeface-hero-lg-font-weight);
		font-size: var(--typography-typescale-hero-lg-font-size);
		letter-spacing: var(--typography-typescale-hero-lg-letter-spacing);
		line-height: var(--typography-typescale-hero-lg-line-height);
	}
</style>

<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HeadingTags, Size } from '../index.js';

	type TypographyHeroProps = {
		children: Snippet;
		tag: HeadingTags;
		size: Size;
	};

	let { children, tag = 'h1', size = 'md' }: TypographyHeroProps = $props();

	let typographyClasses = `typography-title-${size}`;
</script>

<svelte:element this={tag} class={typographyClasses}>
	{#if children}
		{@render children()}
	{/if}
</svelte:element>

<style>
	.typography-title-sm {
		font-family: var(--typography-typeface-title-sm-font-family);
		font-weight: var(--typography-typeface-title-sm-font-weight);
		font-size: var(--typography-typescale-title-sm-font-size);
		letter-spacing: var(--typography-typescale-title-sm-letter-spacing);
		line-height: var(--typography-typescale-title-sm-line-height);
	}
	.typography-title-md {
		font-family: var(--typography-typeface-title-md-font-family);
		font-weight: var(--typography-typeface-title-md-font-weight);
		font-size: var(--typography-typescale-title-md-font-size);
		letter-spacing: var(--typography-typescale-title-md-letter-spacing);
		line-height: var(--typography-typescale-title-md-line-height);
	}
	.typography-title-lg {
		font-family: var(--typography-typeface-title-lg-font-family);
		font-weight: var(--typography-typeface-title-lg-font-weight);
		font-size: var(--typography-typescale-title-lg-font-size);
		letter-spacing: var(--typography-typescale-title-lg-letter-spacing);
		line-height: var(--typography-typescale-title-lg-line-height);
	}
</style>

<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { TextTags, Size } from '../index.js';

	type TypographyLabelProps = {
		children: Snippet;
		tag: TextTags;
		size: Size;
	};

	let { children, tag = 'p', size = 'md' }: TypographyLabelProps = $props();

	let typographyClasses = `${size}`;
</script>

<svelte:element this={tag} class={typographyClasses}>
	{#if children}
		{@render children()}
	{/if}
</svelte:element>

<style>
	.sm {
		font-family: var(--typography-typeface-label-sm-font-family);
		font-weight: var(--typography-typeface-label-sm-font-weight);
		font-size: var(--typography-typescale-label-sm-font-size);
		letter-spacing: var(--typography-typescale-label-sm-letter-spacing);
		line-height: var(--typography-typescale-label-sm-line-height);
	}
	.md {
		font-family: var(--typography-typeface-label-md-font-family);
		font-weight: var(--typography-typeface-label-md-font-weight);
		font-size: var(--typography-typescale-label-md-font-size);
		letter-spacing: var(--typography-typescale-label-md-letter-spacing);
		line-height: var(--typography-typescale-label-md-line-height);
	}
	.lg {
		font-family: var(--typography-typeface-label-lg-font-family);
		font-weight: var(--typography-typeface-label-lg-font-weight);
		font-size: var(--typography-typescale-label-lg-font-size);
		letter-spacing: var(--typography-typescale-label-lg-letter-spacing);
		line-height: var(--typography-typescale-label-lg-line-height);
	}
</style>

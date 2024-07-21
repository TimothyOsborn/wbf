<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { TextTags, Size } from '../index.js';

	type TypographyBodyProps = {
		children: Snippet;
		tag: TextTags;
		size: Size;
	};

	let { children, tag = 'p', size = 'md' }: TypographyBodyProps = $props();

	let typographyClasses = `typography-body-${size}`;
</script>

<svelte:element this={tag} class={typographyClasses}>
	{#if children}
		{@render children()}
	{/if}
</svelte:element>

<style>
	.typography-body-sm {
		font-family: var(--typography-typeface-body-sm-font-family);
		font-weight: var(--typography-typeface-body-sm-font-weight);
		font-size: var(--typography-typescale-body-sm-font-size);
		letter-spacing: var(--typography-typescale-body-sm-letter-spacing);
		line-height: var(--typography-typescale-body-sm-line-height);
	}
	.typography-body-md {
		font-family: var(--typography-typeface-body-md-font-family);
		font-weight: var(--typography-typeface-body-md-font-weight);
		font-size: var(--typography-typescale-body-md-font-size);
		letter-spacing: var(--typography-typescale-body-md-letter-spacing);
		line-height: var(--typography-typescale-body-md-line-height);
	}
	.typography-body-lg {
		font-family: var(--typography-typeface-body-lg-font-family);
		font-weight: var(--typography-typeface-body-lg-font-weight);
		font-size: var(--typography-typescale-body-lg-font-size);
		letter-spacing: var(--typography-typescale-body-lg-letter-spacing);
		line-height: var(--typography-typescale-body-lg-line-height);
	}
</style>

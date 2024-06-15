<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HTMLButtonAttributes } from 'svelte/elements';

	type ButtonProps = {
		children: Snippet;
		href?: string;
		action?: any;
		type?: HTMLButtonAttributes['type'];
	};

	let { children, href, action, type = 'button' }: ButtonProps = $props();

	let buttonClasses: string =
		'flex ai-center bg-transparent color-primary padding-md border br-md jc-center min-width-120 text-decoration-none';
</script>

{#if href}
	<a {href} class={buttonClasses} role="button">
		{#if children}
			{@render children()}
		{/if}
	</a>
{:else}
	<button {type} class={buttonClasses} onclick={action}>
		{#if children}
			{@render children()}
		{/if}
	</button>
{/if}

<style>
	a,
	button {
		display: inline-flex;
		box-sizing: border-box;
		align-items: center;
		background-color: transparent;
		color: #0e9f6e;
		padding: 8px 16px;
		border: 2px solid #0e9f6e;
		font-family:
			system-ui,
			'Open Sans',
			-apple-system,
			sans-serif;
		font-size: 16px;
		line-height: 24px;
		justify-content: center;
		border-radius: 8px;
		text-decoration: none;
		transition: all 0.5s;
		box-shadow: 0px 1px 3px 0px #888;
	}
</style>

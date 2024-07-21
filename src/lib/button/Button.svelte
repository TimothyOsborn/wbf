<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HTMLButtonAttributes } from 'svelte/elements';
	import type { Size } from '../index.js';

	type ButtonProps = {
		children: Snippet;
		href?: string;
		action?: any;
		primary?: string;
		size?: Size;
		shape?: string;
		type?: HTMLButtonAttributes['type'];
	};

	let {
		children,
		href,
		action,
		size = 'md',
		shape = 'none',
		type = 'button',
		color = 'primary'
	}: ButtonProps = $props();

	let buttonClasses: string = `elevation-effect elevation-2 typography-label-${size} colors-${color} ${size}`;
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
		display: inline-block;
		padding: var(--_button-padding-vertical, 8px) var(--_button-padding-horizontal, 16px);
		text-decoration: none;
		border: none;
		appearance: none;

		&.sm {
			--_button-padding-vertical: 6px;
			--_button-padding-horizontal: 12px;
		}
		&.lg {
			--_button-padding-vertical: 10px;
			--_button-padding-horizontal: 20px;
		}
	}
	a:active,
	button:active {
		--_elevation-box-shadow-color: var(--colors-primary);
	}
</style>

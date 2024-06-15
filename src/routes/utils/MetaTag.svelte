<script lang="ts">
	import { MetaTags } from 'svelte-meta-tags';
	export let description: string = '';
	export let title: string = '';
	let breadcrumb_title = title.toLowerCase().replaceAll(' ', '-');
</script>

<MetaTags title={breadcrumb_title} titleTemplate="%s - Work by Flow" {description} />

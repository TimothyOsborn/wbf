<script lang="ts">
	import Button from '$lib/button/Button.svelte';
	const log = () => console.log('panda');
</script>

<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<Button href="www.google.com">Apply now</Button>
<Button action={log}>Apply now</Button>

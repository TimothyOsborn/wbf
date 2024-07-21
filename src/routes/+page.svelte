<script lang="ts">
	import Button from '$lib/button/Button.svelte';
	import TypographyBody from '$lib/typography/TypographyBody.svelte';
	import TypographyLabel from '$lib/typography/TypographyLabel.svelte';
	import TypographyHero from '$lib/typography/TypographyHero.svelte';
	import TypographyTitle from '$lib/typography/TypographyTitle.svelte';
	import '$lib/css/index.css';
	const log = () => console.log('panda');
</script>

<Button href="www.google.com">Apply now</Button>
<Button action={log} size="sm">Apply now</Button>
<Button action={log} size="md">Apply now</Button>
<Button action={log} size="lg">Apply now</Button>
<Button action={log} color="secondary" size="md">Apply now</Button>
<Button action={log} color="tertiary" size="md">Apply now</Button>
<Button action={log} color="error" size="md">Apply now</Button>
<TypographyLabel>
	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
	labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat.
</TypographyLabel>
<TypographyBody>
	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
	labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat.
</TypographyBody>
<TypographyTitle>
	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
	labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat.
</TypographyTitle>
<TypographyHero>
	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
	labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat.
</TypographyHero>

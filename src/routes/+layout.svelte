<script lang="ts">
	import '../app.postcss';
	import NavBar from '$lib/components/NavBar.svelte';
	import { AppShell } from '@skeletonlabs/skeleton';
</script>

<NavBar />

<slot />

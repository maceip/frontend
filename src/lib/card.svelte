<script lang="ts">
	import Button from './button.svelte';
	import type { ButtonI } from './types';
	export let title: string;
	export let buttons: ButtonI[] = [];
</script>

<div class="m-4 px-5 py-4 text-center bg-body-tertiary rounded-2">
	<h2 class="text-body-emphasis m-3">{title}</h2>
	<div class="col-lg-8 mx-auto fs-5 text-muted">
		<slot />
	</div>
	<div class="d-inline-flex gap-5 my-3">
		{#each buttons as button}
			<Button link={button.link} cls={button.cls} text={button.text} />
		{/each}
	</div>
</div>

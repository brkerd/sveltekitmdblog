<script lang="ts">
	import { formatDate } from '$lib/utils';

	export let data;
</script>

<article>
	<hgroup>
		<h1 class="font-heading text-text">{data.meta.title}</h1>
		<p class="font-body text-text/70">Published at {formatDate(data.meta.date)}</p>
	</hgroup>

	<div class="flex gap-3 my-3">
		{#each data.meta.categories as category}
			<span class="p-1 border rounded-md font-body font-bold"> &num;{category} </span>
		{/each}
	</div>

	<div>
		<svelte:component this={data.content} />
	</div>
</article>

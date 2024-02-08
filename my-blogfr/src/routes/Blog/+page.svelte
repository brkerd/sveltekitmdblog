<script lang="ts">
	import { formatDate } from '$lib/utils';

	export let data;
</script>

<section>
	<ul class="grid gap-8">
		{#each data.posts as post}
			<a href="/Blog/{post.slug}">
				<li class=" border rounded-md shadow-md hover:shadow-sm hover:border-primary/50">
					<h2 class="text-primary font-heading ml-2">{post.title}</h2>
					<p class="ml-2 my-1 font-body text-text/70">{formatDate(post.date)}</p>
					<p class="ml-2 my-1 font-body">{post.description}</p>
				</li>
			</a>
		{/each}
	</ul>
</section>

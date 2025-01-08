<script>
	let { title, description, tags, stars, url, commitamount } = $props();
</script>

<div class="w-full border-2 border-dashed border-primary p-4">
	<h3>{title}</h3>

	<p>{description}</p>

	<div class="mt-4">
		<div class="mt-4 flex justify-between items-center">
			<span>{commitamount} commits</span><a href={url} class="link" target="_blank">Bekijk op GitHub</a>
		</div>

        <div class="flex flex-wrap gap-1">
            {#each tags as tag}
                <span class="badge badge-primary">{tag}</span>
            {/each}
        </div>

		<!-- <span>{stars} sterren</span> -->
	</div>
</div>

<script>
	let {children, href, title } = $props();

	const scrollToBottom = async (node) => {
		node.scroll({ top: node.scrollHeight, behavior: 'smooth' });
	};
</script>

<a
	{href}
	onclick={() => {
		scrollToBottom(document.getElementById(href.split('#')[0]));
	}}
	class="card bg-primary shadow-xl"
>
	<div class="card-body">
		<h2 class="card-title headerlink">{title}</h2>
		{@render children()}
	</div>
</a>

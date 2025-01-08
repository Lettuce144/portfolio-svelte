<script>
	import Projectcard from '../../components/projects/projectcard.svelte';
	import { _ } from 'svelte-i18n';

	let repos = [];
	let filteredRepos = [];
	let activeFilter = null;

	const filters = {
		All: () => repos,
		Frontend: () => repos.filter((repo) => repo.language === 'JavaScript'),
		Backend: () => repos.filter((repo) => repo.topics.includes('backend')),
		Fullstack: () =>
			repos.filter((repo) => repo.topics.includes('fullstack', 'frontend', 'backend')),
		Games: () => repos.filter((repo) => repo.topics.includes('games')),
		Misc: () => repos.filter((repo) => repo.topics.includes('misc'))
	};

	try {
		fetch('https://api.github.com/users/Lettuce144/repos')
			.then((res) => res.json())
			.then((data) => {
				repos = data.filter((repo) => repo.topics.includes('portfolio'));
				applyFilter('All');
			});
	} catch (error) {
		console.error(error);
	}

	function applyFilter(key) {
		activeFilter = key;
		filteredRepos = filters[key]();

		console.log(activeFilter);
	}
</script>

<div class="border-2 border-dashed border-primary p-4">
	<h3 class="sectionheader">{$_('Projects_Page_Title')}</h3>

	<div class="flex flex-row flex-wrap gap-1">
		{#each Object.keys(filters) as key}
			<button
				class="btn btn-primary {activeFilter === key ? 'btn-disabled' : ''}"
				on:click={() => applyFilter(key)}
			>
				{key}
			</button>
		{/each}
	</div>

	<div class="mt-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
		{#each filteredRepos as repo}
			<Projectcard
				title={repo.name}
				description={repo.description}
				tags={[repo.language]}
				stars={repo.stargazers_count}
				url={repo.html_url}
				commitamount="69"
			/>
		{/each}
	</div>
</div>

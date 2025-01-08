<script>
	import Experienceblock from '../../components/experienceblock.svelte';
	import { _ } from 'svelte-i18n';
	import { redirect } from '@sveltejs/kit';

	let tools = [
		'Visual Studio & (Code)',
		'Blender',
		'Git',
		'Docker',
		'Vue.js',
		'React',
		'Node.js',
		'ASP.NET'
	];

	let programmingLanguages = [
		'C++',
		'C#',
		'HTML',
		'CSS',
		'JavaScript',
		'PHP',
		'SQL',
		'Java',
		'Python',
		'Lua'
	];


</script>

<div class="border-2 border-dashed border-primary p-4">
	<h3 id="title">{$_('Work_title')}</h3>

	<p class="md:w-3/4">
		{$_('Work_cv_why')}
	</p>

	<div class="mt-4">
		<a href="/cv" class="btn btn-primary">{$_('Work_cv_download')}</a>
	</div>

	<h3>{$_('Work_timeline')}</h3>

	{#if 0}
		<ul class="timeline timeline-vertical lg:timeline-horizontal">
			<li>
				<div class="timeline-start">1984</div>
				<div class="timeline-middle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="h-5 w-5"
					>
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
							clip-rule="evenodd"
						/>
					</svg>
				</div>
				<div class="timeline-end timeline-box">First Macintosh computer</div>
				<hr />
			</li>
			<li>
				<hr />
				<div class="timeline-start">1998</div>
				<div class="timeline-middle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="h-5 w-5"
					>
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
							clip-rule="evenodd"
						/>
					</svg>
				</div>
				<div class="timeline-end timeline-box">iMac</div>
				<hr />
			</li>
			<li>
				<hr />
				<div class="timeline-start">2001</div>
				<div class="timeline-middle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="h-5 w-5"
					>
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
							clip-rule="evenodd"
						/>
					</svg>
				</div>
				<div class="timeline-end timeline-box">iPod</div>
				<hr />
			</li>
			<li>
				<hr />
				<div class="timeline-start">2007</div>
				<div class="timeline-middle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="h-5 w-5"
					>
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
							clip-rule="evenodd"
						/>
					</svg>
				</div>
				<div class="timeline-end timeline-box">iPhone</div>
				<hr />
			</li>
			<li>
				<hr />
				<div class="timeline-start">2015</div>
				<div class="timeline-middle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="h-5 w-5"
					>
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
							clip-rule="evenodd"
						/>
					</svg>
				</div>
				<div class="timeline-end timeline-box">Apple Watch</div>
			</li>
		</ul>
	{/if}
	<Experienceblock
		title="Stage"
		place="Bedrijf"
		yearStart="2023-11"
		yearEnd="2024-08"
		experienceType="Work"
	>
		Als onderdeel van mijn opleiding heb ik stage gelopen bij een bedrijf. Hier heb ik onderzoek
		gedaan naar de mogelijkheden van een nieuwe technologie en heb ik een proof-of-concept gemaakt.
	</Experienceblock>

	<Experienceblock
		title="Stage"
		place="Bedrijf"
		yearStart="2023-11"
		yearEnd="2024-08"
		experienceType="Education"
	>
		Als onderdeel van mijn opleiding heb ik stage gelopen bij een bedrijf. Hier heb ik onderzoek
		gedaan naar de mogelijkheden van een nieuwe technologie en heb ik een proof-of-concept gemaakt.
	</Experienceblock>
</div>

<div class="mt-4 gap-4 flex flex-col md:flex-row justify-between">
	<div class="border-2 w-full md:w-1/3 border-dashed border-primary p-4">
		<h3>{$_('Work_lang')}</h3>
		<ul class="list-disc list-inside">
			<li>{$_('NL')}: {$_('Lang_perfect')}</li>
			<li>{$_('EN')}: {$_('Lang_perfect')}</li>
			<li>{$_('DE')}: {$_('Lang_reasonble')}</li>
		</ul>
	</div>
	<div class="border-2 w-full md:w-1/3 border-dashed border-primary p-4">
		<h3>{$_('Work_program_lang')}</h3>
		<div class="flex flex-wrap gap-1">
			{#each programmingLanguages as language}
				<span class="badge badge-primary">{language}</span>
			{/each}
		</div>
	</div>
	<div class="border-2 w-full md:w-1/3 border-dashed border-primary p-4">
		<h3>{$_('Work_Tools')}</h3>
		<div class="flex flex-wrap gap-1">
			{#each tools as tool}
				<span class="badge badge-primary">{tool}</span>
			{/each}
		</div>
	</div>
</div>

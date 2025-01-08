<script>
	import Headerblock from './headerblock.svelte';
	import { _ } from 'svelte-i18n';
</script>

<!-- Contains all of the elements that make up the header -->

<h1>{$_('Home_Title')}</h1>
<p>
	{$_('Home_About_01')}

	<br />
	<br />

    {$_('Home_About_02')}
</p>

<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4 p-0 m-0 mt-4">
	<Headerblock title={$_('MyWork')} href="/work#title">
		{$_('MyWork_Description')}
	</Headerblock>

	<Headerblock title={$_('Projects')} href="/projects">
		{$_('Projects_Description')}
	</Headerblock>

	<Headerblock title={$_('Contact_Block')} href="/contact">
		{$_('Contact_Description')}
	</Headerblock>

	<Headerblock title={$_('About')} href="/about">
		{$_('About_Description')}
	</Headerblock>
</div>

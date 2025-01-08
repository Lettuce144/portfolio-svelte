<script>
	import { _ } from "svelte-i18n";
</script>

<div class="w-full border-2 border-dashed border-primary p-4">
	<div class="flex w-full flex-col gap-2">
		<div class="collapse collapse-arrow bg-base-200">
			<input type="radio" checked name="my-accordion-2" />
			<div class="collapse-title text-xl font-medium">{$_("About_Work_Title")}</div>
			<div class="collapse-content">
				<p>{@html $_("About_Work")}</p>
			</div>
		</div>
		<div class="collapse collapse-arrow bg-base-200">
			<input type="radio" name="my-accordion-2" />
			<div class="collapse-title text-xl font-medium">{$_("About_Sector_Title")}</div>
			<div class="collapse-content">
				<p>{$_("About_Sector")}</p>
			</div>
		</div>
	</div>
</div>

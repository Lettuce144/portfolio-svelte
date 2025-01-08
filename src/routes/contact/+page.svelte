<script>
	import { _ } from 'svelte-i18n';
</script>

<div class="w-full border-2 border-dashed border-primary p-4 flex flex-col md:flex-row gap-8">
	<!-- Contact Form -->
	<div class="md:w-1/2 flex flex-col gap-4">
		<h3 class="sectionheader font-bold">{$_('Contact_Page_Title')}</h3>

		<form class="flex flex-col gap-4">
			<!-- Name Input -->
			<div>
				<label for="name" class="label font-semibold">{$_('Contact_Page_name')}:</label>
				<input id="name" type="text" class="input input-bordered w-full" placeholder="John doe" />
			</div>

			<!-- Email Input -->
			<div>
				<label for="email" class="label font-semibold">{$_('Contact_Page_email')}:</label>
				<input
					id="email"
					type="email"
					class="input input-bordered w-full"
					placeholder="doejohn@mail.com"
				/>
			</div>

			<!-- Message Textarea -->
			<div>
				<label for="textarea" class="label font-semibold">{$_('Contact_Page_message')}:</label>
				<textarea id="textarea" class="textarea textarea-bordered w-full" placeholder="Msg here..."
				></textarea>
			</div>

			<!-- Submit Button -->
			<button
				class="btn btn-primary w-full"
				on:click={() => {
					const name = document.getElementById('name').value;
					const email = document.getElementById('email').value;
					const message = document.getElementById('textarea').value;
					const mailtoLink = `mailto:zeefjens@gmail.com?subject=Vraag%20-%20Zakelijk&body=${encodeURIComponent(message)}`;
					window.location.href = mailtoLink;
				}}
			>
				{$_('Contact_Page_send')}
			</button>
		</form>
	</div>

	<div class="divider md:divider-horizontal divider-vertical"></div>

	<!-- Contact Information -->
	<div class="md:w-1/2 flex flex-col justify-center gap-4">
		<p class="font-bold text-lg">{$_('Contact_Page_subtitle')}</p>
		<ul class="list-none flex flex-col gap-1">
			<li>
				<a href="https://www.linkedin.com" class="link link-primary">LinkedIn</a>
			</li>
			<li>
				<a href="https://www.youtube.com" class="link link-primary">YouTube</a>
			</li>
			<li>
				<a href="https://www.github.com" class="link link-primary">GitHub</a>
			</li>
		</ul>

		<p class="text-gray-700">
			<strong>Email:</strong>
			<a href="mailto:zeefjens@gmail.com" class="link link-primary">zeefjens@gmail.com</a>
		</p>
		<p class="text-gray-700">
			<strong>{$_('Contact_Page_place')}</strong> Groningen, Netherlands
		</p>
	</div>
</div>

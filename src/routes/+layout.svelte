<script lang="ts">
	import '../app.css';

	import { EnvelopeIcon, GithubLogoIcon, IconContext, RssIcon, XLogoIcon } from 'phosphor-svelte';

	import { resolve } from '$app/paths';

	import BlueskyIcon from '$lib/components/BlueskyIcon.svelte';
	import Search from '$lib/components/Search.svelte';

	let { children } = $props();
</script>

<IconContext values={{ size: 24 }}>
	<header class="flex w-full justify-center">
		<div class="flex w-full max-w-7xl justify-between p-4">
			<a class="btn font-mono text-2xl tracking-widest btn-ghost" href={resolve('/')}>
				<img src="/avatar.jpeg" class="size-9" alt="my avatar" />
				Bahaa Zidan
			</a>
			<Search />
		</div>
	</header>

	{@render children()}

	<footer class="mt-auto flex w-full justify-center bg-neutral">
		<div class="footer w-full max-w-7xl items-center p-4 text-neutral-content sm:footer-horizontal">
			<aside class="grid-flow-col items-center">
				<p>Thank you for reading!</p>
			</aside>
			<nav class="grid-flow-col gap-4 md:place-self-center md:justify-self-end">
				<IconContext
					values={{
						size: 24,
						class: 'transition-all duration-300 ease-in-out hover:text-gray-900',
					}}
				>
					<a
						href={resolve('/rss.xml')}
						target="_blank"
						aria-label="RSS"
						data-umami-event="Follow"
						data-umami-event-target="RSS"
					>
						<RssIcon />
					</a>
					<a
						href="mailto:io@bahaazidan.com"
						aria-label="Email"
						data-umami-event="Follow"
						data-umami-event-target="Email"
					>
						<EnvelopeIcon />
					</a>
					<a
						href="https://github.com/BahaaZidan"
						target="_blank"
						rel="nofollow"
						aria-label="GitHub"
						data-umami-event="Follow"
						data-umami-event-target="GitHub"
					>
						<GithubLogoIcon />
					</a>
					<a
						href="https://x.com/GebnaTorky"
						target="_blank"
						rel="nofollow"
						aria-label="Twitter"
						data-umami-event="Follow"
						data-umami-event-target="Twitter"
					>
						<XLogoIcon />
					</a>
					<a
						href="https://bsky.app/profile/bahaazidan.com"
						target="_blank"
						rel="nofollow"
						aria-label="Bluesky"
						data-umami-event="Follow"
						data-umami-event-target="Bluesky"
					>
						<BlueskyIcon />
					</a>
				</IconContext>
			</nav>
		</div>
	</footer>
</IconContext>

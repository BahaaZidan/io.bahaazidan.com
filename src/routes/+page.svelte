<script lang="ts">
	import { IconContext } from 'phosphor-svelte';
	import { siCloudflare, siGraphql, siReact, siSvelte, siTypescript } from 'simple-icons';

	import { resolve } from '$app/paths';

	import BrandIcon from '$lib/components/BrandIcon.svelte';
	import Head from '$lib/components/Head.svelte';
	import { DEFAULT_DESCRIPTION, DEFAULT_TITLE } from '$lib/constants';
</script>

<Head
	title={DEFAULT_TITLE}
	description={DEFAULT_DESCRIPTION}
	pathname="/"
	imagePath="/avatar.jpeg"
/>

<main class="flex flex-col items-center">
	<div class="relative h-150 w-full bg-[url(/hero.webp)] bg-cover bg-center">
		<div class="absolute inset-0 bg-linear-to-b from-transparent via-transparent to-base-100"></div>
	</div>
	<div class="relative -top-20 -mb-20 size-40 rounded-full bg-[url(/avatar.jpeg)] bg-contain"></div>
	<div class="mx-3 my-2 flex max-w-xl flex-col gap-4">
		<div class="text-center font-mono text-3xl font-semibold text-primary-content">Bahaa Zidan</div>
		<div class="text-center text-primary-content/50">App Development Consultant/Freelancer</div>
		<div class="text-secondary-content/80">
			<IconContext values={{ class: 'size-4.5' }}>
				I build apps, open source software, teach programming, write articles, and make videos. My
				areas of focus are: <span class="badge"><BrandIcon icon={siTypescript} />TypeScript</span>
				<span class="badge"><BrandIcon icon={siCloudflare} />Serverless</span>
				<span class="badge"><BrandIcon icon={siGraphql} />GraphQL</span>
				<span class="badge"><BrandIcon icon={siReact} />React Native</span>
				<span class="badge"><BrandIcon icon={siSvelte} />Svelte</span>
			</IconContext>
		</div>
		<div class="text-secondary-content/80">
			I'm currently building <span class="badge font-mono font-bold">Kelma</span>
			A fediverse connected content platform that's built around user intent. So instead of click-baits
			and adverstisments, it offers a one-press monetization model that is dead-simple for the viewer
			and much more sustainable for the content creater.
		</div>
		<div class="flex justify-center gap-2">
			<div class="tooltip" data-tip="Soon">
				<button class="btn" disabled>Checkout Kelma</button>
			</div>
			<a href={resolve('/blog')} class="btn">Read my blog</a>
			<a href="mailto:io@bahaazidan.com" class="btn">Hire me</a>
		</div>
	</div>
</main>

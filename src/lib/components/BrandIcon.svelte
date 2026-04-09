<script lang="ts">
	import { SquareIcon } from 'phosphor-svelte';
	import type { SimpleIcon } from 'simple-icons';

	interface Props {
		icon: SimpleIcon;
	}

	const { icon }: Props = $props();
</script>

<SquareIcon weight="fill" color="transparent">
	<g transform="scale(10.6666667)">
		<path d={icon.path} fill="currentColor" />
	</g>
</SquareIcon>

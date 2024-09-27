<script>
	import Icon from '@iconify/svelte';
	import { fade } from 'svelte/transition';

	const infos = [
		{
			time: '2023-Present',
			title: 'Software Developer',
			subtitle: 'Font-End Web3 Developer',
			description:
				'Participated in developing front-end experience with Web3 design and integration of smart contract. Integrating UI and UX for seamless user friendly application.'
		},
		{
			time: '2022-2023',
			title: 'Junior Web Developer',
			subtitle: 'Dashboard Design and Development',
			description:
				'Develop dashboard for crypto transaction, customer request with CRUD design. User role based design for dashboard permission access.'
		}
	];
</script>

<div in:fade class="grid grid-cols-2 gap-5">
	{#each infos as info}
		<div class="flex flex-col gap-5 p-6 border border-gray-300/70 rounded-xl">
			<div class="flex items-center gap-2 text-primary">
				<Icon icon="mdi:calculator" width="1.2em" height="1.2em" />
				<div class="">
					{info.time}
				</div>
			</div>
			<div class="font-semibold h3">
				{info.title}
			</div>

			<div class="font-semibold text-[#696969]">
				{info.subtitle}
			</div>

			<div class="text-[#696969] font-thin">
				{info.description}
			</div>
		</div>
	{/each}
</div>

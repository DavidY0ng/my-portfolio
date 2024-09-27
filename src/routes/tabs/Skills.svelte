<script>
	import { fade } from 'svelte/transition';

	const infos = [
		{ name: 'Svelte', img: '1', value: '98' },
		{ name: 'Tailwind', img: '2', value: '98' },
		{ name: 'NodeJs', img: '3', value: '90' },
		{ name: 'HTML & CSS', img: '4', value: '96' },
		{ name: 'Javascript', img: '5', value: '95' },
		{ name: 'React', img: '6', value: '90' },
		{ name: 'NestJS', img: '7', value: '85' },
		{ name: 'Postgres', img: '8', value: '85' }
	];
</script>

<div in:fade class="grid grid-cols-4 gap-10 justify-items-center">
	{#each infos as info}
		<div
			class="bg-[#262629] h-[310px] w-[220px] rounded-full flex flex-col items-center justify-center hover:grayscale-0 grayscale transition duration-500"
		>
			<div class="mb-10">
				<img src="/logo/{info.img}.png" class="" />
			</div>
			<div class="mb-2 text-white h2">
				{info.value}%
			</div>
			<div class="text-base text-white">
				{info.name}
			</div>
		</div>
	{/each}
</div>

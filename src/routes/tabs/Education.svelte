<script>
	import Icon from '@iconify/svelte';
	import { fade } from 'svelte/transition';

	const infos = [
		{
			time: '2022',
			title: 'Full Stack Web Development Certificate',
			subtitle: 'NEXT Academy',
			description:
				'This certification from NEXT Academy equipped me with comprehensive skills in both front-end and back-end development. Through a rigorous curriculum and hands-on projects, I gained expertise in creating dynamic, responsive web applications.'
		},
		{
			time: '2012',
			title: 'Bachelor of Science in Psychology',
			subtitle: 'Sunway University',
			description:
				'My academic journey at Sunway University provided me with a strong foundation in understanding human behavior and cognitive processes. The knowledge gained from this program continues to inform my approach to creating engaging and effective digital experiences.'
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

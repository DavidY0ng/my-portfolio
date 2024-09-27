<script>
	import { fade } from 'svelte/transition';

	const infos = [
		{ title: 'name', value: 'David Yong Chee Ho' },
		{ title: 'nationality', value: 'Malaysian' },
		{ title: 'phone', value: '+60 12 693 6437' },
		{ title: 'email', value: 'yongcheeho@gmail.com' },
		{ title: 'experience', value: '2 years' },
		{ title: 'freelance', value: 'Available' },
		{ name: 'language', value: 'English, Chinese, Malay, Cantonese' }
	];
</script>

<div in:fade class="mx-auto w-[550px] flex flex-col gap-10">
	<h3 class="font-semibold h3">Software Developer</h3>
	<p class="font-thin">
		Hello, I'm David, a seasoned product developer with a passion for crafting innovative solutions.
		I've honed my skills over years of hands-on experience in the industry, specializing in creating
		user-centric products that exceed expectations. Let's collaborate and bring your ideas to life!
	</p>
	<div class="grid w-full grid-cols-1 gap-1">
		{#each infos as info}
			<div class="grid grid-cols-[120px,50px,200px]">
				<div class="capitalize">
					{info.title}
				</div>
				<div class="">:</div>
				<div class="font-semibold">
					{info.value}
				</div>
			</div>
		{/each}
	</div>
</div>

<script lang="ts">
	import Title from '../lib/components/Title.svelte';
	import { TabGroup, Tab, TabAnchor } from '@skeletonlabs/skeleton';
    import AboutMe from './tabs/AboutMe.svelte';
    import Icon from '@iconify/svelte';
   
	let tabSet: number = 0;

	const tabs = [
		{ name: 'about me', icon: 'bi:inbox' },
		{ name: 'experience', icon: 'ph:compass' },
		{ name: 'education', icon: 'icon-park-solid:degree-hat' },
		{ name: 'skills', icon: 'ion:rocket-outline' }
	];
</script>

<div class="relative bg-[#f8f9f9] h-[50vh] min-h-[800px]">
	<div class="w-full max-w-[1200px] mx-auto py-[100px]">
		<Title section="resume" title="My Resume" />
        <div class="flex justify-center mt-10">
            <TabGroup border="border-none" active="border-none bg-primary " padding="p-5" class="w-[900px]">
                <div class="w-full flex justify-between capitalize font-semibold bg-[#EBB884]/40 rounded-full">
                    {#each tabs as tab,i}
                        <Tab bind:group={tabSet} name={tab.name} value={i} class="w-[220px] text-lg flex justify-center" rounded="rounded-full">
                            <div class="flex items-center gap-3">
                                <span><Icon icon={tab.icon} width="1.2em" height="1.2em" /></span>{tab.name}
                            </div>
                            
                        </Tab>
                    {/each}
                </div>
    
                <!-- Tab Panels --->
                <svelte:fragment slot="panel">
                    {#if tabSet === 0}
                        <AboutMe/>
                    {:else if tabSet === 1}
                        (tab panel 2 contents)
                    {:else if tabSet === 2}
                        (tab panel 3 contents)
                    {/if}
                </svelte:fragment>
            </TabGroup>
        </div>
		
	</div>
</div>

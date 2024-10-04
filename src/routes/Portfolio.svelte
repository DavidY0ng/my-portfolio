<script>
    import Title from "../lib/components/Title.svelte";

    const infos = [
        {title: "Skywalker Lab", subtitle: "Company branch landing page", img: "01", link:"https://skywalker-lab.netlify.app/"},
        {title: "Skywalker Tech", subtitle: "Web3 tech multiple pages site", img: "02", link:"https://skywalker-tech.netlify.app/"},
        {title: "Bujing Web", subtitle: "Customer's Web3 community landing page", img: "03", link:"https://bujing.netlify.app/"},
        {title: "Chain Party", subtitle: "Client's Web3 Game Project", img: "04", link:"https://chainparty.xyz/game"},
        {title: "Redacted", subtitle: "Client's NFT Landing Page", img: "05", link:"https://redacted-landing.netlify.app/"}
    ]
</script>

<div class="relative bg-white h-[900px]">
    <div class="w-full max-w-[1130px] mx-auto py-[100px]">
        <Title title="My Work" section="portfolio"/>
        <div class="grid grid-cols-3 gap-4 mt-10 justify-items-center">
            {#each infos as info}
            <a class="relative overflow-hidden rounded-lg card group" href={info.link} target="_blank">
                <!-- Image: Added transition for scaling on hover -->
                <img src="/portfolio/{info.img}.png" class="inset-0 z-0 object-cover transition-transform duration-1000 group-hover:scale-110" alt="portfolio_img">
                
                <!-- Gradient and Text Container -->
                <div class="absolute inset-0 z-10 flex flex-col items-start justify-center transition-opacity duration-1000 opacity-0 group-hover:opacity-100">
                    <!-- Gradient Background -->
                    <div class="absolute inset-0 bg-gradient-to-b from-[#EBB884] to-[#1d1d1d] opacity-80 z-0"></div>
                    
                    <!-- Title and Subtitle -->
                    <div class="relative z-10 w-full pl-5">
                        <div class="bg-[#1d1d1d] text-white p-1 px-3 rounded-md text-lg font-bold mb-2 hover:text-primary w-1/2">
                            {info.title}
                        </div>
                        <div class="bg-[#1d1d1d] text-white p-1 px-3 rounded-md hover:text-primary w-3/4">
                            {info.subtitle}
                        </div>
                    </div>
                </div>
            </a>
            {/each}
        </div>
    </div>
</div>
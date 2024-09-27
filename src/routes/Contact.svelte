<script>
    const socialLinks = [
        {name: "linkedin", link: 'https://www.linkedin.com/in/david-yong-5a1532103/'},
        {name: "github", link: 'https://github.com/DavidY0ng'},
        {name: "instagram", link: 'https://www.instagram.com/david_ych/'}
    ]
</script>

<div class="relative h-[400px] bg-[#1d1d1d]">
    <div class="w-full max-w-[1200px] mx-auto">
        <div class="flex justify-center gap-20 pt-[100px]">
            <div class="flex flex-col gap-4">
                <div class="text-lg font-bold text-white">
                     Say Hello
                </div>
                <div class="text-white">
                     yongcheeho@gmail.com
                </div>
                <div class="text-2xl font-semibold text-primary">
                     +6012 693 6437
                </div>
             </div>
             <div class="flex flex-col gap-4">
                <div class="text-lg font-bold text-white">
                    Social
                </div>
                <div class="flex flex-col gap-2 font-semibold uppercase">
                    {#each socialLinks as link}
                        <a href={link.link} target="_blank" class="text-white hover:text-[#EBB884] transition-colors duration-500">
                            {link.name}
                        </a>
                    {/each}
                </div>
                
             </div>
        </div>
        
        
    </div>
    
</div>
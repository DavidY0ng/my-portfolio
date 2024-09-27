<script>
    const paths = [
        {name: "home", path:'#home'},
        {name: "about me", path:'#resume'},
        {name: "work", path:'#work'},
        {name: "contact", path:'#contact'}
    ]
</script>

<div class="fixed p-5 bg-white/50 shadow-sm z-[999] w-full">
    <div class="w-full max-w-[1200px] mx-auto">
        <div class="flex justify-end gap-8 font-semibold">
            {#each paths as path}
            <a class="uppercase hover:text-[#EBB884] transition-all duration-300" href={path.path}>
                {path.name}
            </a>
            {/each}
        </div>
    </div>
</div>


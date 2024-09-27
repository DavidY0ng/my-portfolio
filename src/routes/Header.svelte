<script>
    const paths = [
        {name: "home", path:''},
        {name: "about me", path:''},
        {name: "work", path:''}
    ]
</script>
<div class="bg-white shadow-sm sticky p-5">
    <div class="w-full max-w-[1200px] mx-auto">
        <div class="flex gap-8 font-semibold justify-end">
            {#each paths as path}
            <a class="uppercase hover:text-[#EBB884] transition-all duration-300" href="#"> {path.name}</a>
            {/each}
        </div>
    </div>
</div>


<script lang='ts'>
	import { Bell, EnvelopeClosed, Home, MagnifyingGlass, PaperPlane, Reader } from "radix-icons-svelte";
    const sidebarOptions = [
        {
            icon:Home,
            title:'home',
            href:'/'
        },
        {
            icon:MagnifyingGlass,
            title:'explorer',
            href:'/'
        },
        {
            icon:Bell,
            title:'notification',
            href:'/'
        },
        {
            icon:EnvelopeClosed,
            title:'messages',
            href:'/'
        },
        {
            icon:Reader,
            title:'lists',
            href:'/'
        },
        {
            icon:PaperPlane,
            title:'communities',
            href:'/'
        },
    ]
</script>

<section class="px-3 md:flex-[0.2] md:px-2 border flex justify-between flex-col sticky z-10 top-0 left-0">
    <div class="mt-10">

        {#each sidebarOptions as {icon, title, href} }
            <a {href} class="flex gap-[22px] p-3 w-fit rounded-full hover:bg-white/10"> 
                <svelte:component this={icon} class="w-7 h-7"/>
                <p class="text-lg capitalize hidden md:inline-block pr-5">{title}</p>
            </a>
        {/each}
    </div>
</section>
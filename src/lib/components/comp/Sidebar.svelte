<script lang='ts'>
	import { Bell, Bookmark, EnvelopeClosed, Home, MagnifyingGlass, PaperPlane, Pencil1, Reader, ThickArrowLeft } from "radix-icons-svelte";
	import Button from "../ui/button/button.svelte";
	import * as Avatar from "$lib/components/ui/avatar";
	import Progress from "../ui/progress/progress.svelte";
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
        {
            icon: Bookmark,
            title:'primium',
            href:'/'
        },
        {
            icon:ThickArrowLeft,
            title:'logout',
            href:'/'
        },
    ]
</script>

<section class="px-3 md:flex-[0.2] h-screen md:px-2 border flex justify-between flex-col sticky z-10 top-0 left-0">
    <div class="mt-10">

        {#each sidebarOptions as {icon, title, href} }
            <a {href} class="flex gap-[22px] p-3 w-fit rounded-full hover:bg-white/10"> 
                <svelte:component this={icon} class="w-7 h-7"/>
                <p class="text-lg capitalize hidden md:inline-block pr-5">{title}</p>
            </a>
        {/each}
    </div>

    <Button class="md:py-6 md:w-full">
        <Pencil1 class="md:mr-2 h-4 w-4"/>
        <span class="hidden md:inline">Post</span>
    </Button>

    <div class='flex gap-2 items-center justify-center'>
        <Avatar.Root>
            <Avatar.Image src="https://raw.githubusercontent.com/sphade/twitter-clone/main/static/xLogo.svg">
                <Avatar.Fallback>
                    US
                </Avatar.Fallback>
            </Avatar.Image>
        </Avatar.Root>

        <div class="hidden md:inline-block">
            <p class="font-medium capitalize">Md. Tahuruzzoha Tuhin</p>
            <p class="text-gray-600"> tzz.tuhin@gmail.com</p>
        </div>
    </div>
</section>
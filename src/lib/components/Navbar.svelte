<script>
    import Icon from '@iconify/svelte';
    import jsLogo from '$lib/data/jsLogo.svg?raw';

    let menuOpen = false;
    
    const handleClose = () => {
        menuOpen = false
        if (document.body.classList.contains("noScroll")) {
            document.body.classList.remove("noScroll")
        }
    }

    const handleMenu = () => {
        menuOpen = !menuOpen

        if (document.body.classList.contains("noScroll")) {
            document.body.classList.remove("noScroll")
        }
        else {
            document.body.classList.add("noScroll")
        }
    }
</script>

<div class="w-screen fixed nav h-[90px] z-40 flex justify-center">
    <div class="w-full centered text-white flex justify-between items-center h-[90px] fixed max-w-[1200px] px-5">
        <a class="font-bold min-w-[175px] text-xl duration-300 ease-in-out transition-all md:hover:scale-[103%] md:hover:drop-shadow-[0_0_0.25rem_#61BEFF]" href="/" on:click={() => handleClose()}>
            {@html jsLogo}
        </a>
        <ul class="lg:flex hidden text-lg font-semibold">
            <a href="/" on:click={() => handleClose()}><li class="px-4 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0000:</span> Home</li></a>
            <a href="projects" on:click={() => handleClose()}><li class="px-4 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0001:</span> Projects</li></a>
            <a href="experience" on:click={() => handleClose()}><li class="pl-4 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0010:</span> Experience</li></a>
        </ul>
    
        <!-- Hamburger menu -->
        <button class={`lg:hidden text-[35px] transition-all ease-in-out rounded-xl duration-150 ${!menuOpen ? '' : 'bg-[#0b0b0b] p-3'}`} on:click={() => handleMenu()} >
            <Icon icon="lucide:menu" />
        </button>
    </div>
</div>

{#if menuOpen}
    <button class={`${menuOpen ? 'left-0' : 'left-[-100%]'} lg:hidden z-20 overflow-x-hidden overflow-y-hidden w-full cursor-auto h-screen fixed top-0 left-0 bg-[#222222]/50`} on:click={() => handleMenu()}></button>
{/if}

<div class={`transition-all z-30 text-[125%] uppercase nav font-semibold min-w-[250px] text-white lg:hidden ease-in-out duration-300 ${menuOpen ? 'right-0' : 'md:right-[-40%] right-[-250px]'} fixed pt-[90px] w-[250px] top-0 md:w-[40%] h-full border-l border-gray-600`}>
    <ul class="text-left font-bold">
        <a href="/" on:click={() => handleClose()}>
            <li class="p-5 border-b border-gray-600 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0000:</span> Home</li>
        </a>
        <a href="projects" on:click={() => handleClose()}>
            <li class="p-5 border-b border-gray-600 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0001:</span> Projects</li>
        </a>
        <a href="experience" on:click={() => handleClose()}>
            <li class="p-5 border-b border-gray-600 duration-150 ease-in-out transition-all hover:text-[#61BEFF]"><span class="text-[#61BEFF]">0010:</span> Experience</li>
        </a>
    </ul>
</div>
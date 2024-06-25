<script>
    import "../app.css";
    import { onMount } from "svelte";
    import Navbar from "../lib/components/Navbar.svelte";
    import jsIcon from '$lib/data/icon.svg?raw';

    let animation = true
    let grow = true
    onMount(async () => {
        const delay = ms => new Promise(res => setTimeout(res, ms));
        document.body.classList.add('overflow-y-hidden');
        await delay(500)
        grow = false
        await delay(500)
        grow = true 
        await delay(1000)
        grow = false
        animation = false
        document.body.classList.remove('overflow-y-hidden');
    })

</script>

<div class={`${animation ? 'top-0 left-0 opacity-100 z-[70]' : 'opacity-0 z-[-1]'} bg-black text-3xl font-bold flex justify-center items-center duration-300 ease-in-out transition-all w-screen h-full fixed`}>
    <h1 class={`${grow ? 'scale-100 drop-shadow-[0_0_0rem_#61BEFF]' : 'drop-shadow-[0_0_0.75rem_#61BEFF] scale-[120%]'} duration-[700ms] ease-in-out transition-all w-1/2 md:w-1/6 drop-shadow-[0_0_0.75rem_#61BEFF]`}>{@html jsIcon}</h1>
</div>

<Navbar />
<div class="w-full h-auto">
    <div class="mx-auto max-w-[1200px] px-5">
        <slot />
    </div>
</div>

<div class="w-full h-auto min-h-[200px] drop-shadow-[0_0_0.35rem_black] bg-[#222222]">
    <div class="mx-auto flex w-full h-full flex-col items-center justify-center max-w-[600px] px-5 text-white">
        <div class="flex text-[20px] pb-[20px] pt-[20px] justify-around items-start w-full">
            <div class="flex flex-col justify-center px-[30px] items-start">
                <h1 class="font-bold text-[#61BEFF] uppercase">Navigation</h1>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" href="/">Home</a>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" href="projects">Projects</a>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" href="experience">Experience</a>
            </div>

            <div class="flex flex-col justify-center px-[30px] items-start">
                <h1 class="font-bold text-[#61BEFF] uppercase">Social Media</h1>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" target="_blank" href="https://github.com/Jxk0be">GitHub</a>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" target="_blank" href="https://www.linkedin.com/in/jake-shoffner/">LinkedIn</a>
                <a class="md:hover:scale-[103%] md:hover:text-[#61BEFF] duration-300 transition-all ease-in-out" target="_blank" href="https://www.instagram.com/ijxke_s/">Instagram</a>
            </div>
        </div>
        <h1 class="pb-[20px]">© 2024 Jake Shoffner. All rights reserved.</h1>
    </div>
</div>
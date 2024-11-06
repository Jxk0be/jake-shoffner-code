<script>
    import { reveal } from 'svelte-reveal'
    import jsIcon from '$lib/data/icon.svg?raw';
    import Typewriter from 'svelte-typewriter'
</script>

<div class="w-full flex flex-col h-auto items-center md:min-h-0 pb-[30px] pt-[100px]">
    <h1 class="w-[100px] bg-[#222222] rounded-[50%] p-3"><h1 class="duration-300 ease-in-out transition-all md:hover:scale-[103%] md:hover:drop-shadow-[0_0_0.25rem_#61BEFF]">{@html jsIcon}</h1></h1>
    <h1 class="font-semibold text-2xl md:text-4xl pt-[10px] text-center">Hello! I'm <span class="font-semibold text-[#61BEFF] font-['Poppins']">Jake Shoffner</span>.</h1>
    <div class="flex pb-[20px] min-w-[200px] flex-row justify-center items-center md:text-2xl text-xl md:font-bold font-bold drop-shadow-[0px_10px_15px_rgba(0,0,0,0.75)]">
        &#8205;
        <h1>I'm a&nbsp;</h1>
        <Typewriter mode="loop" interval={[66, 76, 74, 70, 63, 54, 63, 64, 74, 64]} cursor={false}>
            <h1 class="text-[#61BEFF]">Software Engineer...</h1>
            <h1 class="text-[#61BEFF]">Graphic Designer...</h1>
            <h1 class="text-[#61BEFF]">Problem Solver...</h1>
        </Typewriter>
    </div>
    <p class="md:text-xl text-lg leading-[1.75rem] pb-4">
        I'm currently working on some exciting things over at
        <a class="text-[#61BEFF] font-semibold hover:text-[#4E98CC] transition-all duration-300 ease-in-out" href="https://pilotflyingj.com/" target="_blank">Pilot</a>.
        Mostly working with SvelteKit on the frontend side of things. I'm also working on fun small projects all the time, you should definitely 
        check out my Github!
    </p>
    <p class="md:text-xl text-lg leading-[1.75rem] pb-4">
        This website is a reimagining of my old React site I made when I was first Learning
        web development. Some major differences in this website: page routing (<span class="italic">thanks</span>
        <a class="text-[#61BEFF] font-semibold hover:text-[#4E98CC] transition-all duration-300 ease-in-out" href="https://kit.svelte.dev/" target="_blank">SvelteKit</a> 😎),
        new personal branding, more mobile-friendly design, and waaaaaaay faster &#x1F3C3 (<span class="italic">thanks again Svelte!!</span>).
    </p>
    <p class="md:text-xl text-lg leading-[1.75rem]">
        Well, I think I've bored you long enough. Please enjoy my website and look around all you want.
        You can see some cool projects, you can learn a little bit about my journey, and finally, you can reach out to me
        on social media if you ever want to chat!
    </p>
</div>

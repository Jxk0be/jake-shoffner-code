<script>
    import { reveal } from 'svelte-reveal'
    import Budget from "$lib/data/Budget-app.png"
    import YT from "$lib/data/YT-block.png"
    import PokerAI from "$lib/data/poker-ai.png"
    import ChessAI from "$lib/data/chess-ai.png"
    import Transcript from "$lib/data/transcript.png"
    import { fly } from 'svelte/transition'
</script>

<div class="w-full flex flex-col h-auto items-center md:min-h-0 pb-[30px] md:text-2xl text-xl pt-[100px]">
    <h1 class="font-semibold text-2xl md:text-4xl pt-[10px] text-center pb-[40px] font-['Poppins']">My Projects</h1>
    <div class="flex justify-center w-full h-full">
        <div class="w-full md:w-[80%] pb-[30px] flex flex-col items-center gap-[40px]">

            <div class="flex flex-col justify-center md:justify-between items-center w-full md:pb-[40px] pb-[20px] md:h-[700px]">
                <div in:fly={{ delay: 400, y: 20, duration: 2400}} class="overflow-hidden min-h-[100px] relative w-full max-h-[360px] md:max-h-[100%] md:mb-[15px] mb-[10px] rounded-xl">
                    <a class="flex justify-center items-center h-full" href="https://github.com/COSC401-Neural-Net-Poker" target="_blank"><img class="duration-[1200ms] ease-in-out transition-all md:hover:scale-[105%] object-cover object-center" alt="poker" src={PokerAI} /></a>
                </div>
    
                <div class="w-full text-white md:h-auto min-h-[200px] md:max-h-[400px]">
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Full Stack
                        </div>
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] ml-3 uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Machine Learning
                        </div>
                    </div>
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <h1 use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="w-full flex items-start font-bold md:text-3xl text-2xl">Bluff Buddy Poker AI Web Application (2024)</h1>
                    </div>
                    <p use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="text-gray-300">
                        My Senior Design group project at the University of Tennessee, Knoxville. This project was to create an
                        interactive poker AI to play against, via a web application. Some technologies used include: React,
                        Firebase, Flask, and PyTorch.
                    </p>
                </div>
            </div>

            <div class="flex flex-col justify-center md:justify-between items-center w-full md:pb-[40px] pb-[20px] md:h-[700px]">
                <div in:fly={{ delay: 400, y: 20, duration: 2400}} class="overflow-hidden min-h-[100px] relative w-full max-h-[360px] md:max-h-[100%] md:mb-[15px] mb-[10px] rounded-xl">
                    <a class="flex justify-center items-center h-full" href="https://github.com/utk-cs340-fall22/Chess" target="_blank"><img class="duration-[1200ms] ease-in-out transition-all md:hover:scale-[105%] object-cover object-center" alt="chess" src={ChessAI} /></a>
                </div>
    
                <div class="w-full text-white md:h-auto min-h-[200px] md:max-h-[400px]">
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Full Stack
                        </div>
                    </div>
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <h1 use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="w-full flex items-start font-bold md:text-3xl text-2xl">Chess Engine Web Application (2022)</h1>
                    </div>
                    <p use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="text-gray-300">
                        This group project was my introduction to full stack development and
                        working within a team. Our mission was straightforward: create a web-based
                        chess bot. The catch? We were clueless about transitioning C++ code from the
                        terminal to the web. And thus, our learning journey began.
                    </p>
                </div>
            </div>

            <div class="flex flex-col justify-center md:justify-between items-center w-full md:pb-[40px] pb-[20px] md:h-[700px]">
                <div in:fly={{ delay: 400, y: 20, duration: 2400}} class="overflow-hidden min-h-[100px] relative w-full max-h-[360px] md:max-h-[100%] md:mb-[15px] mb-[10px] rounded-xl">
                    <a class="flex justify-center items-center h-full" href="https://github.com/Jxk0be/YouTube-Metadata-ML-Research-Project" target="_blank"><img class="duration-[1200ms] ease-in-out transition-all md:hover:scale-[105%] object-cover object-center" alt="poster" src={YT} /></a>
                </div>
    
                <div class="w-full text-white md:h-auto min-h-[200px] md:max-h-[400px]">
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Data Science
                        </div>
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] ml-3 uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Machine Learning
                        </div>
                    </div>
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <h1 use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="w-full flex items-start font-bold md:text-3xl text-2xl">YouTube Machine Learning Project (2023)</h1>
                    </div>
                    <p use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="text-gray-300">
                        In this project, we explored defining the parameters of a successful YouTube channel or
                        video. We examined key contributing factors to success and applied regression and
                        classification techniques to gauge their impact, aiming to predict the likelihood
                        of a channel or video achieving success.
                    </p>
                </div>
            </div>

            <div class="flex flex-col justify-center md:justify-between items-center w-full md:pb-[40px] pb-[20px] md:h-[700px]">
                <div in:fly={{ delay: 400, y: 20, duration: 2400}} class="overflow-hidden min-h-[100px] relative w-full max-h-[360px] md:max-h-[100%] md:mb-[15px] mb-[10px] rounded-xl">
                    <a href="https://github.com/Jxk0be/budget-app" target="_blank"><img class="duration-[1200ms] ease-in-out transition-all md:hover:scale-[105%] object-cover object-center w-full h-full" alt="budget" src={Budget} /></a>
                </div>
    
                <div class="w-full text-white md:h-auto min-h-[200px] md:max-h-[400px]">
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            FULL STACK
                        </div>
                    </div>
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <h1 use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="w-full flex items-start font-bold md:text-3xl text-2xl">Budget App & Real-Time Currency Converter (2024)</h1>
                    </div>
                    <p use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="text-gray-300">
                        To celebrate earning my degree, I treated myself to a long-awaited trip to
                        Japan with friends. Wanting to improve my financial management, I embarked
                        on this project. My goal? To track my spending, savings, and integrate a real-time
                        currency converter for seamless travel planning.
                    </p>
                </div>
            </div>

            <div class="flex flex-col justify-center md:justify-between items-center w-full md:pb-[40px] pb-[20px] md:h-[700px]">
                <div in:fly={{ delay: 400, y: 20, duration: 2400}} class="overflow-hidden min-h-[100px] relative w-full max-h-[360px] md:max-h-[100%] md:mb-[15px] mb-[10px] rounded-xl">
                    <a class="flex justify-center items-center h-full" href="https://github.com/Jxk0be/Transcriptified" target="_blank"><img class="duration-[1200ms] ease-in-out transition-all md:hover:scale-[105%] object-cover object-center" alt="transcript" src={Transcript} /></a>
                </div>
    
                <div class="w-full text-white md:h-auto min-h-[00px] md:max-h-[400px]">
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <div use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="bg-[#61BEFF] uppercase text-[15px] tracking-widest font-bold font-['Inter'] h-full px-2 py-[0.1rem] rounded-md">
                            Frontend
                        </div>
                    </div>
                    <div class="flex justify-start items-center w-full mt-[5px] mb-[20px]">
                        <h1 use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="w-full flex items-start font-bold md:text-3xl text-2xl">Transcriptified - A Better Transcript (2022)</h1>
                    </div>
                    <p use:reveal={{ transition: "slide", blur: 20, x: -50, duration: 1200}} class="text-gray-300">
                        Throughout my school years, I found traditional transcripts lacking. I craved
                        customization to make notes for my classes, allowing me to reflect on my courses later with more context.
                        I desired a more visually appealing design to replace the traditional simple text format. Thus,
                        Transcriptified was born!
                    </p>
                </div>
            </div>

        </div>
    </div>
</div>

<script>
    import { fly } from 'svelte/transition'

    let selectedExp = "Pilot"
    let selectedCategory = "Work"
    let selectedEducation = "MS"
</script>

<div class="w-full flex flex-col h-auto items-center md:min-h-0 pb-[30px] md:text-2xl text-xl pt-[100px]">
    <h1 class="font-semibold text-2xl md:text-4xl pt-[10px] text-center pb-[40px] font-['Poppins']">My Experience</h1>
    <div class="flex justify-center w-full h-full">
        <div class="w-full md:w-[80%] pb-[30px] flex flex-col items-center min-w-[300px]">
            <div in:fly={{ delay: 400, y: 20, duration: 1600}} class="w-full mb-4 font-semibold flex md:justify-center justify-between items-center gap-5">
                <button on:click={() => selectedCategory = "Work"} class={`${selectedCategory === "Work" ? 'bg-[#61BEFF] font-bold' : 'bg-[#222222]'} uppercase text-[17px] tracking-widest font-semibold font-['Inter'] h-full md:max-w-[150px] w-full md:w-1/2 md:px-2 py-[0.1rem] rounded-md duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all`}>Work</button>
                <button on:click={() => selectedCategory = "Education"} class={`${selectedCategory === "Education" ? 'bg-[#61BEFF] font-bold' : 'bg-[#222222]'} uppercase text-[17px] tracking-widest font-semibold font-['Inter'] h-full md:max-w-[150px] w-full md:w-1/2 md:px-2 py-[0.1rem] rounded-md duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all`}>Education</button>
            </div>
            {#if selectedCategory === "Work" }
                <div in:fly={{ delay: 400, y: 20, duration: 1600}} class="w-full min-w-[300px] rounded-lg flex md:flex-row flex-col justify-between items-center">
                    <div class="md:w-auto w-full bg-[#222222] h-full rounded-[20px_20px_0_0] md:rounded-[20px_0_0_20px] p-[1rem] text-[18px] items-center flex flex-col md:justify-start">
                        <button on:click={() => selectedExp = "Pilot"} class={`${selectedExp === "Pilot" ? 'bg-[#61BEFF] font-bold' : 'bg-[#131212]'} duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all whitespace-nowrap py-2 mb-4 rounded-[8px] w-full md:w-[250px]`}>Pilot Company</button>
                        <button on:click={() => selectedExp = "KUB"} class={`${selectedExp === "KUB" ? 'bg-[#61BEFF] font-bold' : 'bg-[#131212]'} duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all whitespace-nowrap py-2 mb-4 rounded-[8px] w-full md:w-[250px]`}>Knoxville Utilities Board</button>
                        <button on:click={() => selectedExp = "UTK"} class={`${selectedExp === "UTK" ? 'bg-[#61BEFF] font-bold' : 'bg-[#131212]'} duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all whitespace-nowrap py-2 mb-4 rounded-[8px] w-full md:w-[250px]`}>University of Tennessee</button>
                    </div>
                    <div class="flex text-[18px] flex-col justify-start items-center w-full bg-[#222222] h-full rounded-[0_0_20px_20px] md:rounded-[0_20px_20px_0] p-[1rem]">
                        {#if selectedExp === "Pilot"}
                            <h1 class="font-semibold tracking-wider mb-2">Software Engineer I <a class="company underline" target="_blank" href="https://www.pilotcompany.com/">@Pilot</a></h1>
                            <div class="w-full h-full p-[0.5rem] flex flex-col justify-start items-center">
                                <div class="w-full text-[16px] text-[#d8d6d6] flex flex-col gap-2 px-3">
                                    <li>
                                        Collaborate within an AGILE environment, interfacing with developers,
                                        project managers, stakeholders, designers, and QA testers to deliver top-tier
                                        products.
                                    </li>
                                    <li>
                                        Actively enhance code efficiency and quality to boost performance
                                        and overall user engagement.
                                    </li>
                                </div>
                            </div>
                        {:else if selectedExp === "KUB"}
                            <h1 class="font-semibold tracking-wider mb-2">SWE Student <a class="company underline" target="_blank" href="https://www.kub.org/">@KUB</a></h1>
                            <div class="w-full h-full p-[0.5rem] flex flex-col justify-start items-center">
                                <div class="w-full text-[16px] text-[#d8d6d6] flex flex-col gap-2 px-3">
                                    <li>
                                        Implemented a system within an internal application to
                                        identify and prevent duplicate leave requests for over 1000 employees.
                                    </li>
                                    <li>
                                        Updated Enterprise Java REST APIs to ensure sustained
                                        stability and align with company coding standards.
                                    </li>
                                    <li>
                                        Contributed to our in-house, open-source UI
                                        library for Ember JS applications.
                                    </li>
                                </div>
                            </div>
                        {:else if selectedExp === "UTK"}
                            <h1 class="font-semibold tracking-wider mb-2">Data Science TA <a class="company underline" target="_blank" href="https://www.utk.edu/">@UTK</a></h1>
                            <div class="w-full h-full p-[0.5rem] flex flex-col justify-start items-center">
                                <div class="w-full text-[16px] text-[#d8d6d6] flex flex-col gap-2 px-3">
                                    <li>
                                        Co-conducted weekly lab sessions to better help students
                                        understand data science concepts and practices.
                                    </li>
                                    <li>
                                        Answered and resolved technical problems asked
                                        by students in lab sessions or by email.
                                    </li>
                                </div>
                            </div>
                        {/if}
                    </div>
                </div>
            {:else if selectedCategory === "Education"}
                <div in:fly={{ delay: 400, y: 20, duration: 1600}} class="w-full min-w-[300px] rounded-lg flex md:flex-row flex-col justify-between items-center">
                    <div class="md:w-auto w-full bg-[#222222] h-full rounded-[20px_20px_0_0] md:rounded-[20px_0_0_20px] p-[1rem] text-[18px] items-center flex flex-col md:justify-start">
                        <button on:click={() => selectedEducation = "MS"} class={`${selectedEducation === "MS" ? 'bg-[#61BEFF] font-bold' : 'bg-[#131212]'} duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all whitespace-nowrap py-2 mb-4 rounded-[8px] w-full md:w-[250px]`}>Graduate</button>
                        <button on:click={() => selectedEducation = "BS"} class={`${selectedEducation === "BS" ? 'bg-[#61BEFF] font-bold' : 'bg-[#131212]'} duration-300 ease-in-out hover:font-bold hover:bg-[#61BEFF] transition-all whitespace-nowrap py-2 mb-4 rounded-[8px] w-full md:w-[250px]`}>Undergraduate</button>
                    </div>
                    <div class="flex text-[18px] flex-col justify-start items-center w-full bg-[#222222] h-full rounded-[0_0_20px_20px] md:rounded-[0_20px_20px_0] p-[1rem]">
                        {#if selectedEducation === "BS"}
                            <h1 class="font-semibold tracking-wider whitespace-nowrap">Bachelor of Science in CS</h1>
                            <h1 class="font-semibold tracking-wider mb-2 text-[#d8d6d6] text-[16px]">August 2019 - May 2024</h1>
                            <div class="w-full h-full p-[0.5rem] flex flex-col justify-start items-center">
                                <div class="w-full text-[16px] text-[#d8d6d6] flex flex-col gap-2 px-3">
                                    <li><strong>School:</strong> University of Tennessee, Knoxville</li>
                                    <li><strong>Major:</strong> Computer Science</li>
                                    <li><strong>Minor:</strong> Statistics</li>
                                    <li><strong>Graduation Honors:</strong> Summa Cum Laude</li>
                                    <li><a class="company underline" href="https://aspire.utk.edu/" target="_blank">ASPIRE</a> Scholar</li>
                                </div>
                            </div>
                        {:else if selectedEducation === "MS"}
                            <h1 class="font-semibold tracking-wider whitespace-nowrap">Master of Science in CS</h1>
                            <h1 class="font-semibold tracking-wider mb-2 text-[#d8d6d6] text-[16px]">June 2024 - December 2026</h1>
                            <div class="w-full h-full p-[0.5rem] flex flex-col justify-start items-center">
                                <div class="w-full text-[16px] text-[#d8d6d6] flex flex-col gap-2 px-3">
                                    <li><strong>School:</strong> University of Tennessee, Knoxville</li>
                                    <li><strong>Major:</strong> Computer Science</li>
                                    <li><strong>Concentration:</strong> Data Mining & Intelligent Systems</li>
                                </div>
                            </div>
                        {/if}
                    </div>
                </div>
            {/if}
        </div>
    </div>
</div>

<style>
    .company {
        text-underline-offset: 4px;
        text-decoration-color: #61BEFF;
    }
</style>
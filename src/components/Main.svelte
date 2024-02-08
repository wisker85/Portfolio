<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Placeholder 1', icon: 'fa-solid fa-cookie'},
        {name: 'Placeholder 2', icon: 'fa-solid fa-hand-spock'},
        {name: 'Placeholder 3', icon: 'fa-solid fa-jedi'},
    ];

    let benefits = [
        {name: 'Lorem Ipsum', description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est ad eos ratione magnam debitis perferendis reiciendis rerum quod facilis voluptatibus fugit, maxime iusto similique. Labore nostrum perspiciatis voluptas dicta omnis?'},
        {name: 'Lorem Ipsum', description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est ad eos ratione magnam debitis perferendis reiciendis rerum quod facilis voluptatibus fugit, maxime iusto similique. Labore nostrum perspiciatis voluptas dicta omnis?'},
        {name: 'Lorem Ipsum', description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est ad eos ratione magnam debitis perferendis reiciendis rerum quod facilis voluptatibus fugit, maxime iusto similique. Labore nostrum perspiciatis voluptas dicta omnis?'},
    ];

</script>


<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Ciao! Sono <span class="poppins text-tertiary-400">Andrea</span> Niccolini <br/>Sviluppatore <span class="poppins text-tertiary-400">Full Stack</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Placeholder per una breve descrizione delle mie principali skills
            </p>
            <a href="#" target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins 
                relative overflow-hidden px-6 py-3 group rounded-full variant-filled-primary
                cursor-pointer"
            >
                <div 
                    class="absolute top-0 right-full w-full h-full bg-tertiary-700 opacity-20 
                    group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Contattami &rarr;</h4>    
            </a>
        </div>
        <div class="relative shadow-xl grid place-items-center">
            <img src={"images/profile.png"} alt="Immagine del profilo" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>

    <section id="progetti" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                Alcuni dei miei Progetti.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Volete <span class="poppins text-tertiary-400">vedere</span> i miei lavori?
            </h3>           
        </div>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-primary-100 felx items-center gap-2 -mb-4 
            sm:-mb-0 -mt-10 hover:border-tertiary-700 duration-200"
        >
            <i class="fa-regular fa-circle-play"></i>
            <p>Guarda il video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque, nesciunt saepe vel voluptatem cum dolorum, blanditiis quidem in dignissimos, atque earum provident sed id non? Facilis quisquam quo tempora esse.</p>
            </Step>
            <Step step={steps[1]}>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Natus, provident molestiae. Nostrum neque possimus itaque molestias illum ipsa magni reprehenderit dolorum praesentium corrupti aliquid labore, recusandae unde doloremque quos id?</p>
            </Step>
            <Step step={steps[2]}>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore, deserunt odit? Fugiat quod sint, libero eveniet exercitationem veritatis inventore aliquid consequatur dignissimos similique sequi tenetur corrupti molestias tempora amet id.</p>
            </Step>
        </div>
    </section>
    <section id="profilo" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3
        before:h-1.5 before:bg-tertiary-700 after:absolute after:bottom-0 after:right-0 after:w-2/3
        after:h-1.5 after:bg-tertiary-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Vuoi saperne di più?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">Io sono ...</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-tertiary-400">Complete</span> Package
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="bg-tertiary-700 text-white whitespace-nowrap p-4 px-8"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Critical Thought</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Progamming Ability</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</main>
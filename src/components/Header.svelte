<script>
    export let y;

    let tabs = [
        { name: 'Progetti', link: '#progetti' },
        { name: 'Profilo', link: '#profilo' },
    ];
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center sm:justify-between justify-centerborder border-solid ' + (
    y > 0 ? ' py-4 bg-surface-900 border-tertiary-700' : ' py-6 bg-transparent border-transparent'
)}>
    <h1 class="font-medium">
        Andrea <b class="font-bold">Niccolini</b> 
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab}
            <a href={tab.link} class="duration-200 hover:text-tertiary-600">
                <p>{tab.name}</p>
            </a>
        {/each}
        
        <a href="#" target="_blank" 
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full variant-filled-primary"
            >
            <div 
                class="absolute top-0 right-full w-full h-full variant-filled-tertiary opacity-20 
                group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Contattami</h4>
        </a>
    </div>
</header>
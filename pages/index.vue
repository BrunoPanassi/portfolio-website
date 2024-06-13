<template>
    <div>
        <nav class="bg-gradient-to-r from-slate-900 to-neutral-900 mx-5 px-6 sm:px-4 rounded shadow">
            <div class="container flex flex-wrap justify-between items-center mx-auto">
                <a href="/" class="flex items-center">
                <span class="self-center whitespace-nowrap">
                    <brunoPanassiIcon :size="95" />
                </span>
                </a>

                <div class="flex items-center">
                <button
                    id="menu-toggle"
                    type="button"
                    @click="onToggle"
                    class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600 md:hidden"
                >
                    <!-- Hamburger icon -->
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4 6h16M4 12h16m-7 6h7"
                    />
                    </svg>
                </button>
                </div>

                <div
                class="w-full md:block md:w-auto hidden"
                id="mobile-menu"
                >
                <ul class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium">
                    <li>
                    <a
                        href="#"
                        class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                        aria-current="page"
                    >
                        Home
                    </a>
                    </li>
                    <li>
                    <a
                        href="#"
                        class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                    >
                        Sobre
                    </a>
                    </li>
                    <li>
                    <a
                        href="#"
                        class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                    >
                        Cinco Passos
                    </a>
                    </li>
                    <li>
                    <a
                        href="#"
                        class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                    >
                        Contato
                    </a>
                    </li>
                </ul>
                </div>

            </div>
        </nav>
        <div class="lg:h-screen mt-0 mb-5 mx-5 text-white justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="px-6 py-6 text-center md:px-12 lg:text-left">
                <div class="w-100 2xl:mx-24 lg:my-28 xl:my-32 2xl:my-20">
                    <div class="grid items-center gap-12 lg:grid-cols-2 mb-12">
                        <div class="mt-12 lg:mt-0">
                            <h1 class="mt-2 leading-none lg:leading-tight mb-6 text-5xl font-normal tracking-tight md:text-6xl xl:text-7xl">
                                Sua landing page <br /> <span class="text-primary">que você precisa pra ontem</span>
                            </h1>
                            <h2 class="mt-2 leading-normal mb-6 text-2xl font-light tracking-tight">
                                Com um método baseado em 5 passos
                            </h2>
                            <div class="space-x-4">
                                <button
                                type="button"
                                class="inline-block rounded-lg bg-neutral-950 px-6 pb-2 pt-2.5 text-sm font-medium uppercase leading-normal text-white shadow-primary-3 transition duration-150 ease-in-out hover:bg-primary-accent-300 hover:shadow-primary-2 focus:bg-primary-accent-300 focus:shadow-primary-2 focus:outline-none focus:ring-0 active:bg-primary-600 active:shadow-primary-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong">
                                    + Sobre
                                </button>
                                <button
                                type="button"
                                class="inline-block rounded-lg bg-green-900 px-6 pb-2 pt-2.5 text-sm font-medium uppercase leading-normal text-white shadow-primary-3 transition duration-150 ease-in-out hover:bg-primary-accent-300 hover:shadow-primary-2 focus:bg-primary-accent-300 focus:shadow-primary-2 focus:outline-none focus:ring-0 active:bg-primary-600 active:shadow-primary-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong">
                                    Me interesso
                                </button>
                            </div>
                        </div>
                        <div>
                            <img src="../images/mobile_mockup.jpeg"
                                class="w-full rounded-lg shadow-lg dark:shadow-black/20" alt="" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-stone-900">
            <div class="container mx-auto max-w-5xl flex gap-12 flex-wrap items-start justify-center md:justify-between">
                <div class="grid gap-4 justify-items-center text-center md:flex-1">
                    <div class=" rounded-full border-8 border-amber-900 p-4 ">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-award w-14 h-14"><path d="m15.477 12.89 1.515 8.526a.5.5 0 0 1-.81.47l-3.58-2.687a1 1 0 0 0-1.197 0l-3.586 2.686a.5.5 0 0 1-.81-.469l1.514-8.526"/><circle cx="12" cy="8" r="6"/></svg>
                    </div>
                    <h3 class="text-3xl font-bold">SEO</h3>
                    <p>Otimização para melhorar a sua posição na busca orgânica</p>
                </div>
                <div class="grid gap-4 justify-items-center text-center md:flex-1">
                    <div class=" rounded-full border-8 border-amber-900 p-4 ">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-14 h-14">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z"></path>
                        </svg>
                    </div>
                    <h3 class="text-3xl font-bold">Eficiência</h3>
                    <p>Sua página carregada em menos de 2 segundos.</p>
                </div>
                <div class="grid gap-4 justify-items-center text-center md:flex-1">
                    <div class=" rounded-full border-8 border-amber-900 p-4 ">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-hourglass w-14 h-14"><path d="M5 22h14"/><path d="M5 2h14"/><path d="M17 22v-4.172a2 2 0 0 0-.586-1.414L12 12l-4.414 4.414A2 2 0 0 0 7 17.828V22"/><path d="M7 2v4.172a2 2 0 0 0 .586 1.414L12 12l4.414-4.414A2 2 0 0 0 17 6.172V2"/></svg>

                    </div>
                    <h3 class="text-3xl font-bold">Prioridade</h3>
                    <p>Foco em projetos para quem precisa de uma página pra ontem</p>
                </div>
            </div>
        </div>
        <div class="flex lg:h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
                <div class="max-w-2xl mx-auto text-center">
                    <h2 class="font-heading text-3xl leading-[1.1] md:text-4xl">O método criado para dar foco no seu projeto</h2>
                    <p class="max-w-2xl mx-auto mt-4 text-base text-gray-400 leading-relaxed md:text-2xl">
                        Baseado apenas nesses 5 passos
                    </p>
                </div>
                <div class="relative mt-12 lg:mt-20">
                    <div class="absolute inset-x-0 hidden xl:px-44 top-2 lg:block md:px-20 lg:px-28">
                        <img alt="" loading="lazy" width="1000" height="500" decoding="async" data-nimg="1" class="w-full" style="color:transparent" src="https://cdn.rareblocks.xyz/collection/celebration/images/steps/2/curved-dotted-line.svg">
                    </div>
                    <div class="relative grid grid-cols-1 text-center gap-y-12 lg:grid-cols-5 gap-x-12">
                        <div>
                            <div
                                class="flex items-center justify-center w-16 h-16 mx-auto bg-white border-2 border-gray-200 rounded-full shadow">
                                <span class="text-xl font-semibold text-gray-700">1</span>
                            </div>
                            <h3 class="mt-6 text-xl  text-white font-semibold leading-tight md:mt-10">Briefing</h3>
                            <p class="mt-4 text-base text-gray-400 md:text-lg">
                                A primeira reunião para conhecermos melhor a sua idéia.
                            </p>
                        </div>
                        <div>
                            <div
                                class="flex items-center justify-center w-16 h-16 mx-auto bg-white border-2 border-gray-200 rounded-full shadow">
                                <span class="text-xl font-semibold text-gray-700">2</span>
                            </div>
                            <h3 class="mt-6 text-xl text-white font-semibold leading-tight md:mt-10">Brainstorming</h3>
                            <p class="mt-4 text-base text-gray-400 md:text-lg">
                                Avaliação da sua necessidade no momento e como podemos apresentar a sua marca.
                            </p>
                        </div>
                        <div>
                            <div
                                class="flex items-center justify-center w-16 h-16 mx-auto bg-white border-2 border-gray-200 rounded-full shadow">
                                <span class="text-xl font-semibold text-gray-700">3</span>
                            </div>
                            <h3 class="mt-6 text-xl text-white font-semibold leading-tight md:mt-10">Aprovação</h3>
                            <p class="mt-4 text-base text-gray-400 md:text-lg">
                                Com o projeto aprovado damos início de acordo com a sua urgência
                            </p>
                        </div>
                        <div>
                            <div
                                class="flex items-center justify-center w-16 h-16 mx-auto bg-white border-2 border-gray-200 rounded-full shadow">
                                <span class="text-xl font-semibold text-gray-700">4</span>
                            </div>
                            <h3 class="mt-6 text-xl text-white font-semibold leading-tight md:mt-10">Revisão</h3>
                            <p class="mt-4 text-base text-gray-400 md:text-lg">
                                Assim que o projeto estiver 80% pronto é mostrado para opiniões e devidas alterações
                            </p>
                        </div>
                        <div>
                            <div
                                class="flex items-center justify-center w-16 h-16 mx-auto bg-white border-2 border-gray-200 rounded-full shadow">
                                <span class="text-xl font-semibold text-gray-700">5</span>
                            </div>
                            <h3 class="mt-6 text-xl text-white font-semibold leading-tight md:mt-10">Acompanhamento</h3>
                            <p class="mt-4 text-base text-gray-400 md:text-lg">
                                Após a entrega é feito o acompanhamento durante 7 dias para avaliação de performance.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="h-screen justify-center items-center space-y-6 py-12 md:py-12 lg:py-60 px-12 bg-gradient-to-r from-slate-900 to-stone-900 my-5 mx-5 text-white" v-motion-slide-visible-once-right :delay="500">
            <div class="mx-auto flex max-w-[58rem] flex-col items-center space-y-4 text-center">
                <h2 class="font-heading text-3xl leading-[1.1] sm:text-3xl md:text-4xl">O que posso fazer por você</h2>
                <p class="max-w-[85%] leading-normal text-muted-foreground sm:text-lg sm:leading-7">Qual seria a sua necessidade para o seu negócio.</p>
            </div>
            <div class="mx-auto grid justify-center gap-4 sm:grid-cols-2 md:max-w-[64rem] md:grid-cols-3">
                <div class="relative overflow-hidden rounded-lg lg:border bg-background p-2">
                    <div class="flex h-[180px] flex-col justify-between rounded-md p-6">
                        <svg width="42" height="42" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-mails"><rect width="16" height="13" x="6" y="4" rx="2"/><path d="m22 7-7.1 3.78c-.57.3-1.23.3-1.8 0L6 7"/><path d="M2 8v11c0 1.1.9 2 2 2h14"/></svg>
                        <div class="space-y-2">
                            <h3 class="font-bold">WaitLists</h3>
                            <p class="text-sm text-muted-foreground">Coletar e-mails de leads para o lançamento do seu novo produto.</p>
                        </div>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-lg lg:border bg-background p-2">
                    <div class="flex h-[180px] flex-col justify-between rounded-md p-6">
                        <svg width="42" height="42" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-calendar"><path d="M8 2v4"/><path d="M16 2v4"/><rect width="18" height="18" x="3" y="4" rx="2"/><path d="M3 10h18"/></svg>
                        <div class="space-y-2">
                            <h3 class="font-bold">Agendamento</h3>
                            <p class="text-sm text-muted-foreground">Integração com o calendly para o seu cliente poder agendar com você de forma rápida e ágil.</p>
                        </div>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-lg lg:border bg-background p-2">
                    <div class="flex h-[180px] flex-col justify-between rounded-md p-6">
                        <svg width="42" height="42" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-message-circle"><path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z"/></svg>
                        <div class="space-y-2">
                            <h3 class="font-bold">Redirecionamento para Contato</h3>
                            <p class="text-sm text-muted-foreground">Deixe a melhor forma para que o seu cliente possa contatar você.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-stone-900">
            <div class="mx-auto">
                <div class="max-w-2xl mx-auto text-center">
                    <h2 class="font-heading text-3xl leading-[1.1] md:text-4xl mb-12">Sobre mim</h2>
                </div>
                <div class="card md:flex max-w-3xl">
                    <div class="border rounded-xl h-60 w-60 mx-auto md:mr-6 mb-4 flex-shrink-0 bg-stone-900">
                        <img src="../images/perfil_careca-removebg-preview.png" alt="" />
                    </div>
                    <div class="flex-grow text-center md:text-left">
                        <p class="font-thin text-lg sm:text-2xl">Desenvolvedor Full Stack Pleno</p>
                        <p class="font-bold text-xl sm:text-3xl">bruno.panassi</p>
                        <p class="font-thin text-lg sm:text-3xl mt-2 mb-3">Experiência criando aplicações web para grandes empresas. Expertise em Landing Page com foco em performance.</p>
                        <div class="text-black space-x-2">
                            <button class="text-white border px-3 py-1.5 rounded-lg text-base">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-linkedin"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
                            </button>
                            <button class="text-white border px-3 py-1.5 rounded-lg text-base">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-github"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="mx-auto">
                <div class="card md:flex max-w-3xl divide-x-0 sm:divide-x">
                    <div class="h-60 w-60 mx-auto md:mr-6 flex-shrink-0 text-center flex items-center justify-center">
                        <p class="text-4xl text-semibold">Frameworks, linguagens e ferramentas</p> 
                    </div>
                    <div class="flex-grow text-center px-4 mb-4 space-y-2">
                        <div v-for="(stack) of techByStacks">
                            <p class="font-thin text-lg sm:text-xl mb-2">
                                {{ stack.stack }}
                            </p>
                            <div class="flex items-center justify-center space-x-2" >
                                <Icon 
                                    v-for="(tech) of stack.techs" 
                                    :name="tech"
                                />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="mx-auto">
                <div class="mt-24 card max-w-3xl">
                    <div class=" mx-auto text-center items-center justify-center">
                        <p class="text-4xl text-semibold">Agende uma call</p>
                        <p class="text-lg font-thin">Vamos bater um papo e entender mais sobre, sem compromisso.</p> 
                        <button class="mt-6 space-x-2 bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded inline-flex items-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-calendar"><path d="M8 2v4"/><path d="M16 2v4"/><rect width="18" height="18" x="3" y="4" rx="2"/><path d="M3 10h18"/></svg>
                            <CalendlyPopupButton v-bind="calendlyOptions" :root-element="roofElement"/>
                        </button>
                    </div>
                    <div ref="roofElement"></div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="mx-auto">
                <div class="mt-24 card max-w-3xl">
                    <div class="mx-auto text-center items-center justify-center">
                        <p class="text-4xl text-semibold">Ou se preferir, fale comigo</p>
                        <p class="text-lg font-thin">Tire a sua idéia do papel.</p> 
                        <button class="mt-6">
                            <Icon name="mdi:whatsapp" size="42"/>
                        </button>
                        <a href="https://wa.me/5518997648833?text=Oi!%20Estou%20interessado%20em%20seus%20servi%C3%A7os%20e%20gostaria%20de%20saber%20mais%20sobre%20isso.%20Voc%C3%AA%20poderia%20me%20enviar%20mais%20informa%C3%A7%C3%B5es?%20Obrigado!" target="_blank">Clique</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="justify-center items-center my-5 mx-5 bg-gradient-to-r from-slate-900 to-stone-900 icon px-5 py-12" ref="professionalExperience" v-motion-slide-visible-once-bottom :delay="500">
            <!-- TW Elements is free under AGPL, with commercial license required for specific uses. See more details: https://tw-elements.com/license/ and contact us for queries at tailwind@mdbootstrap.com --> 
            <div class="max-w-2xl my-12 mx-auto text-center">
                <h2 class="font-heading text-3xl leading-[1.1] md:text-4xl">Experiência</h2>
                <p class="max-w-2xl mx-auto mt-4 text-base text-gray-400 leading-relaxed md:text-2xl">
                    Por onde eu trabalhei e quais foram os resultados
                </p>
            </div>
            <ol class="px-6 lg:px-24">
                <li v-for="(work) of professionalExperienceTimeline" v-motion-slide-visible-once-left>
                    <div class="flex-start flex items-center pt-3">
                    <div class="-ml-[5px] mr-3 h-[9px] w-[9px] rounded-full bg-neutral-300 dark:bg-neutral-500"></div>
                    <p class="text-sm text-neutral-500 dark:text-neutral-300">
                        {{ work.date }}
                    </p>
                    </div>
                    <div class="mb-6 ml-4 mt-2">
                        <h4 class="mb-1.5 text-xl font-bold">{{ work.company }}</h4>
                        <p class="mb-3 text-xl font-semibold text-neutral-200 dark:text-neutral-300">
                            Responsibilities:
                        </p>
                        <p class="mb-3 text-xl text-neutral-500 dark:text-neutral-300" style="white-space: pre-wrap;">
                           {{ work.responsibilities }}
                        </p>
                        <p class="mb-3 text-xl font-semibold text-neutral-200 dark:text-neutral-300">
                            Results:
                        </p>
                        <p class="mb-3 text-xl text-neutral-500 dark:text-neutral-300" style="white-space: pre-wrap;">
                           {{ work.results }}
                        </p>
                    </div>
                </li>
            </ol>
        </div>
        <div class="flex h-screen justify-center items-center font-sans my-5 mx-5 bg-gradient-to-r from-slate-900 to-stone-900" ref="aboutNowBlock" v-motion-slide-visible-once-left :delay="500">
            <div class="text-left px-10">
                <button v-for="(value, index) of aboutMeButtons" @click="selectAboutMe(index)" :class="getBackgroundOnSelectedButton(index)">
                    {{ value.text }}
                </button>
                <p class="mt-5 text-lg font-normal text-zinc-50" style="white-space: pre-wrap; line-height: 1.6;">{{ selectedParagraph }}</p>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center my-5 mx-5 bg-gradient-to-r from-slate-900 to-stone-900 icon" ref="stacks" v-motion-slide-visible-once-right :delay="500">
            <div class="text-left px-10">
                <p class="text-lg font-semibold text-zinc-50">Main Stacks</p>
                <div class="flex flex-wrap justify-center mt-2 space-x-2">
                    <div class="flex text-base space-x-2 mt-2 px-2 chip" v-for="(stack) of stackIcons">
                        <div class="py-1">
                            <Icon :name="stack.icon" color="black"/>
                        </div>
                        <span class="py-2">{{ stack.text }}</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center my-5 mx-5 bg-gradient-to-r from-slate-900 to-stone-900 icon px-5 py-12" ref="projects" v-motion-slide-visible-once-right :delay="500">
            <div
                class="block rounded-lg p-6 bg-neutral-800">
                <div class="inline-flex items-center justify-between w-full">
                    <h5
                        class="mb-2 text-xl font-medium leading-tight text-neutral-800 dark:text-neutral-50">
                        text-to-carousel
                    </h5>
                    <a class="mb-4" href="https://github.com/BrunoPanassi/text_to_carousel" target="_blank" rel="noopener noreferrer">
                        <Icon name="mdi:github"/>
                    </a>
                </div>
                <p class="mb-4 text-base text-neutral-600 dark:text-neutral-200">
                    Create images to instagram/linkedin carousel from simple texts
                </p>
                <div class="inline-flex items-center justify-between w-full">
                    <div>
                        <Icon name="vscode-icons:file-type-vue" size="26px" />
                        <Icon name="devicon:vuetify" size="26px"/>
                        <Icon name="vscode-icons:file-type-nuxt" size="26px"/>
                        <Icon name="skill-icons:typescript" size="26px"/>
                    </div>
                    <a class="mb-4" href="https://text-to-carousel.vercel.app/" target="_blank" rel="noopener noreferrer">
                        <button
                            type="button"
                            class="inline-block rounded bg-green-800 px-6 pb-2 pt-2.5 text-xs font-medium uppercase leading-normal text-white "
                            data-te-ripple-init
                            data-te-ripple-color="light">
                            Demo
                        </button>
                    </a>
                </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center my-5 mx-5 bg-gradient-to-r from-slate-900 to-stone-900 icon px-5 py-12" ref="others" v-motion-slide-visible-once-bottom :delay="500">
            <div>
                <a class="mr-2" href="https://dev.to/brunopanassi" target="_blank" rel="noopener noreferrer">
                    <Icon name="fa6-brands:dev" size="42px"/>
                </a>
                <a href="https://stackoverflow.com/users/15636147/brunopanassi" target="_blank" rel="noopener noreferrer">
                    <Icon name="devicon:stackoverflow" size="42px"/>
                </a>
            </div>
        </div>
</template>

<script setup lang="ts">
import { computed } from 'vue';
import brunoPanassiIcon from "~/icons/brunoPanassiIcon.vue"

function onToggle() {
    const mobileMenu = document.getElementById('mobile-menu');
    mobileMenu?.classList.toggle('hidden');
}

const aboutNowBlock = ref<HTMLDivElement>();
const stacks = ref<HTMLDivElement>();
const professionalExperience = ref<HTMLDivElement>();
const projects = ref<HTMLDivElement>();
const others = ref<HTMLDivElement>();

const roofElement = ref()

const calendlyOptions = {
    url: 'https://calendly.com/bhenrique95?hide_gdpr_banner=1',
    text: "Agendar"
}

const mainLinks = [
    {
        ref: "https://www.linkedin.com/in/bruno-henrique-bb3a19141/?locale=en_US",
        icon: "mdi:linkedin"
    },
    {
        ref: "https://github.com/BrunoPanassi",
        icon: "mdi:github"
    },
    {
        ref: "mailto:bhenrique95@outlook.com",
        icon: "mdi:email"
    }
]

const secundaryLinks = [
    {
        goTo: "about-now",
        title: "ABOUT"
    },
    {
        goTo: "stacks",
        title: "STACKS"
    },
    {
        goTo: "professional-experience",
        title: "PROFESSIONAL EXPERIENCE"
    },
    {
        goTo: "projects",
        title: "PROJECTS"
    },
    {
        goTo: "others",
        title: "OTHERS"
    }
]

const techByStacks = [
    {
        stack: "Linguagens",
        techs: [
            "akar-icons:javascript-fill",
            "akar-icons:typescript-fill",
            "ri:java-fill",
            "akar-icons:python-fill",
            "akar-icons:node-fill"
        ]
    },
    {
        stack: "Frameworks",
        techs: [
            "mdi:vuejs",
            "mdi:nuxt",
            "mdi:vuetify",
            "simple-icons:quasar",
            "mdi:tailwind",
            "bxl:spring-boot"
        ]
    },
    {
        stack: "Banco de Dados",
        techs: [
            "simple-icons:postgresql",
            "simple-icons:mysql",
            "fontisto:oracle"
        ]
    },
    {
        stack: "Ferramentas",
        techs: [
            "mdi:docker",
            "mdi:git",
            "solar:figma-bold",
            "mage:photoshop"
        ]
    }
]

const stackIcons = [
    {
        text: "Vue.js",
        icon: "vscode-icons:file-type-vue"
    },
    {
        text: "Vuetify",
        icon: "devicon:vuetify"
    },
    {
        text: "Vite",
        icon: "vscode-icons:file-type-vite"
    },
    {
        text: "Pinia",
        icon: "logos:pinia"
    },
    {
        text: "Nuxt",
        icon: "vscode-icons:file-type-nuxt"
    },
    {
        text: "Quasar",
        icon: "vscode-icons:file-type-light-quasar"
    },
    {
        text: "Javascript",
        icon: "skill-icons:javascript"
    },
    {
        text: "Typescript",
        icon: "skill-icons:typescript"
    },
    {
        text: "Tailwind",
        icon: "vscode-icons:file-type-tailwind"
    },
    {
        text: "Java",
        icon: "devicon:java"
    },
    {
        text: "JUnit",
        icon: "simple-icons:junit5"
    },
    {
        text: "Spring Boot",
        icon: "devicon:spring"
    },
    {
        text: "Postgres",
        icon: "logos:postgresql"
    }
]

const aboutMeButtons = [
    {
        id: 0,
        text: "Myself",
        paragraph: "As a full stack web developer I've helped companies in the car rental, real estate, agriculture and water treatment businesses build and maintain their web applications legible and scalable for this last 6 years.\nI tend to be someone who can solve bugs in legacy systems and ongoing projects, coming up with ideas for improvements and refactoring the code, communicating clearly and having continuous learning."
    },
    {
        id: 1,
        text: "Now",
        paragraph: "Now I'm working at Veolia, where I'm responsible for resolving all bugs, and creating new implementations of the new project made in Vue.js + Quasar.\nI am currently developing an application to help content creators create image carousels to post on their social networks.\nThis project is initially being done with Vue.js, Nuxt, Vuetify, Typescript and Pinia."
    },
    {
        id: 2,
        text: "Future",
        paragraph: "I'm also studying the next technologies I want to learn, such as: Docker, AWS and Kafka.\nI'm looking to evolve into a Senior Developer role and everything I do now is to become one in the future.\nI'm open to working in full stack roles that can open up new opportunities for me to grow with."
    }
]

const professionalExperienceTimeline = [
    {
        date: "01.01.2018 - 01.01.2021",
        company: "FMX Soluções em Tecnologia",
        responsibilities: "Javascript (ES6), Vue.js, Spring Boot, JPA, Hibernate and SQL Server developer on car rent, bovine tract automation and real estate construction systems.",
        results: "On the last client project, was made a executable in Python to convert a spreadsheet to a .txt file, where this file was later used in a software. \nThis task was performed manually and lasted at least 4 hours, after the Python executable conversion, it started to last 10 seconds to execute the whole task."
    },
    {
        date: "01.01.2021 - 01.09.2022",
        company: "Solinftec",
        responsibilities: "Web Developer with Vue.js/Vuetify, Typescript, Spring Boot and Oracle (PL/SQL) on a cane harvest automation project, and currently on a project focused on the logistics and management of the delivery of fungicides and herbicides to the field.",
        results: "On the harvest automation project, a client could receive a loaded truck from another client to fuel your power plant.\nThis information needed to be seen by the two clients at the sametime when its been updated.\nIt was developed with Vue.js Observable and maded some changes in database procedures."
    },
    {
        date: "01.2022 - moment",
        company: "Veolia",
        responsibilities: "Web Developer with Vue.js/Quasar, Spring Boot and Postgres on a water quality treatment project being used in many cities of Brazil and actually in New Zealand.",
        results: "The main system has two interfaces, where the new one was made with Vue.js. All tasks to resolve problems/bugs about the new interface has been send to a new module, and i’amresponsible for the whole module now, to control all the tasks and deliver it in the deadline."
    }
]

let aboutMeButtonSelected = ref(0)

function selectAboutMe(index: number) {
    aboutMeButtonSelected.value = index
}

function getBackgroundOnSelectedButton(index: number) {
    let bgClass = aboutMeButtonSelected.value == index ? 'bg-stone-300 text-black' : 'bg-transparent text-zinc-50'
    return `cursor-pointer ${bgClass} text-lg font-mono py-1 px-2 border border-slate-100 rounded-lg mr-2`
}

const selectedParagraph = computed(() => aboutMeButtons.find((b) => b.id == aboutMeButtonSelected.value)?.paragraph)

const blockRefToGo = [
    {
        id: 'about-now',
        block: aboutNowBlock
    },
    {
        id: 'stacks',
        block: stacks
    },
    {
        id: 'professional-experience',
        block: professionalExperience
    },
    {
        id: 'projects',
        block: projects
    },
    {
        id: 'others',
        block: others
    }
]

useHead({
  htmlAttrs: {
    class: 'html-custom'
  },
  bodyAttrs: {
    class: 'body-custom'
  }
})

function goTo(idSection: string) {
    let block = blockRefToGo.find((b) => b.id == idSection)?.block
    if (block?.value) {
        block.value.scrollIntoView({
            behavior: 'smooth'
        });
    }
    
}

</script>

<style>
.gradient {
	height: 100vh;
	background: linear-gradient(334deg, #6b97f7, #7525e2, #f7137e);
    background-size: 180% 180%;
	animation: gradient-animation 6s ease infinite;
    border-radius: 15px;
}

.section {
    background-color: #17181B;
    border-radius: 15px;
}

.icon {
    font-size: 30px; 
    color: white;
}

.body-custom {
    background-color: #0E1013;
    overflow-x: hidden;
}

.html-custom {
    overflow-x: hidden;
}

.chip {
    border-radius: 15px; 
    width: auto; 
    background-color: white; 
    color: black;
}

@keyframes gradient-animation {
	0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}
</style>
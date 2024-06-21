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
                <ul class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium items-end justify-end">
                    <li>
                    <button
                        class="block py-2 pr-4 pl-3 text-gray-700 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                        @click="goTo('sobre')"
                    >
                        Sobre
                    </button>
                    </li>
                    <li>
                    <button
                        @click="goTo('cinco-passos')"
                        class="block py-2 pr-4 pl-3 text-gray-700 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                    >
                        Cinco Passos
                    </button>
                    </li>
                    <li>
                    <button
                        @click="goTo('cta')"
                        class="block py-2 pr-4 pl-3 text-gray-700 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
                    >
                        Contato
                    </button>
                    </li>
                </ul>
                </div>

            </div>
        </nav>
        <div class="lg:h-screen mt-0 mb-5 mx-5 text-white justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900" ref="home">
            <div class="px-6 py-6 text-center md:px-12 lg:text-left">
                <div class="w-100 2xl:mx-24 lg:my-28 xl:my-32 2xl:my-20">
                    <div class="grid items-center gap-12 lg:grid-cols-2 mb-12">
                        <div class="mt-12 lg:mt-0">
                            <h1 class="mt-2 leading-none lg:leading-tight mb-6 text-5xl font-normal tracking-tight md:text-6xl xl:text-7xl">
                                Sua landing page 
                                <span class="text-primary">
                                    que você precisa <br />pra&nbsp;<span class="typewriter"></span>
                                </span>
                            </h1>
                            <h2 class="mt-2 leading-normal mb-6 text-xl lg:text-2xl font-light tracking-tight">
                                Com um método baseado em 5 passos
                            </h2>
                            <div class="space-x-4">
                                <button
                                type="button"
                                class="inline-block rounded-lg bg-neutral-950 px-6 pb-2 pt-2.5 text-sm font-medium uppercase leading-normal text-white shadow-primary-3 transition duration-150 ease-in-out hover:bg-primary-accent-300 hover:shadow-primary-2 focus:bg-primary-accent-300 focus:shadow-primary-2 focus:outline-none focus:ring-0 active:bg-primary-600 active:shadow-primary-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong"
                                @click="goTo('cinco-passos')">
                                    + Sobre
                                </button>
                                <button
                                type="button"
                                class="inline-block rounded-lg bg-green-900 px-6 pb-2 pt-2.5 text-sm font-medium uppercase leading-normal text-white shadow-primary-3 transition duration-150 ease-in-out hover:bg-primary-accent-300 hover:shadow-primary-2 focus:bg-primary-accent-300 focus:shadow-primary-2 focus:outline-none focus:ring-0 active:bg-primary-600 active:shadow-primary-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong"
                                @click="goTo('cta')">
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
        <div class="flex my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-stone-900">
            <div class="container mx-auto max-w-5xl flex gap-12 flex-wrap items-start justify-center md:justify-between">
                <div class="grid gap-4 justify-items-center text-center md:flex-1">
                    <div class=" rounded-full border-8 border-amber-900 p-4 ">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-award w-14 h-14"><path d="m15.477 12.89 1.515 8.526a.5.5 0 0 1-.81.47l-3.58-2.687a1 1 0 0 0-1.197 0l-3.586 2.686a.5.5 0 0 1-.81-.469l1.514-8.526"/><circle cx="12" cy="8" r="6"/></svg>
                    </div>
                    <h3 class="text-xl font-bold">SEO</h3>
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
                    <h3 class="text-xl font-bold">Performance</h3>
                    <p>Sua página carregada em menos de 2 segundos.</p>
                </div>
                <div class="grid gap-4 justify-items-center text-center md:flex-1">
                    <div class=" rounded-full border-8 border-amber-900 p-4 ">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-hourglass w-14 h-14"><path d="M5 22h14"/><path d="M5 2h14"/><path d="M17 22v-4.172a2 2 0 0 0-.586-1.414L12 12l-4.414 4.414A2 2 0 0 0 7 17.828V22"/><path d="M7 2v4.172a2 2 0 0 0 .586 1.414L12 12l4.414-4.414A2 2 0 0 0 17 6.172V2"/></svg>

                    </div>
                    <h3 class="text-xl font-bold">Prioridade</h3>
                    <p>Foco em projetos para quem precisa de uma página pra ontem</p>
                </div>
            </div>
        </div>
        <div class="flex lg:h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900" ref="cincoPassos">
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
        <div class="justify-center items-center space-y-6 py-12 md:py-12 lg:py-60 px-12 bg-gradient-to-r from-slate-900 to-stone-900 my-5 mx-5 text-white">
            <div class="mx-auto flex max-w-[58rem] flex-col items-center space-y-4 text-center">
                <h2 class="font-heading text-3xl leading-[1.1] sm:text-3xl md:text-4xl">O que posso fazer por você</h2>
                <p class="max-w-[85%] leading-normal text-muted-foreground sm:text-lg sm:leading-7">Qual seria a sua necessidade para o seu negócio.</p>
            </div>
            <div class="mx-auto grid justify-center gap-4 sm:grid-cols-2 md:max-w-[64rem] md:grid-cols-3" v-motion-slide-visible-once-right :delay="500">
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
                            <p class="text-sm text-muted-foreground">Integração com o Calendly para facilitar a sua vida.</p>
                        </div>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-lg lg:border bg-background p-2">
                    <div class="flex h-[180px] flex-col justify-between rounded-md p-6">
                        <svg width="42" height="42" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-message-circle"><path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z"/></svg>
                        <div class="space-y-2">
                            <h3 class="font-bold">Redirecionamento</h3>
                            <p class="text-sm text-muted-foreground">Deixe a melhor forma para que o seu cliente possa contatar você.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex h-screen my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-stone-900" ref="sobre">
            <div class="mx-auto">
                <div class="max-w-2xl mx-auto text-center">
                    <h2 class="font-heading text-3xl leading-[1.1] md:text-4xl mb-12">Sobre mim</h2>
                </div>
                <div class="card md:flex max-w-3xl">
                    <div class="border h-60 w-60 mx-auto md:mr-6 mb-4 flex-shrink-0">
                        <img src="../images/perfil_enhanced.jpeg" alt="" />
                    </div>
                    <div class="flex-grow text-center md:text-left">
                        <p class="font-thin text-lg sm:text-2xl">Desenvolvedor Full Stack Pleno</p>
                        <p class="font-bold text-xl sm:text-3xl">bruno.panassi</p>
                        <p class="font-thin text-lg sm:text-3xl mt-2 mb-3">Experiência criando aplicações web para grandes empresas. Expertise em Landing Page com foco em performance.</p>
                        <div class="text-black space-x-2">
                            <button class="text-white border px-3 py-1.5 rounded-lg text-base">
                                <a href="https://www.linkedin.com/in/bruno-henrique-panassi/" target="_blank" rel="noopener noreferrer">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-linkedin"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
                                </a>
                            </button>
                            <button class="text-white border px-3 py-1.5 rounded-lg text-base">
                                <a href="https://github.com/BrunoPanassi" target="_blank" rel="noopener noreferrer">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-github"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
                                </a>
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
                                    size="24"
                                />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex my-5 mx-5 text-white p-12 lg:py-32 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900">
            <div class="mx-auto">
                <div class="card max-w-3xl">
                    <div class=" mx-auto text-center items-center justify-center">
                        <p class="text-4xl font-semibold">Agende uma call</p>
                        <p class="text-lg font-thin">Vamos bater um papo e entender mais sobre o que você precisa, sem compromisso.</p> 
                        <button class="mt-6 space-x-2 bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded inline-flex items-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-calendar"><path d="M8 2v4"/><path d="M16 2v4"/><rect width="18" height="18" x="3" y="4" rx="2"/><path d="M3 10h18"/></svg>
                            <CalendlyPopupButton v-bind="calendlyOptions" :root-element="roofElement"/>
                        </button>
                    </div>
                    <div ref="roofElement"></div>
                </div>
            </div>
        </div>
        <div class="flex my-5 mx-5 text-white py-32 px-12 lg:p-32 justify-center items-center bg-gradient-to-r from-slate-900 to-neutral-900" ref="cta">
            <div class="mx-auto">
                <div class="card max-w-3xl">
                    <div class="mx-auto text-center items-center justify-center">
                        <p class="text-4xl font-semibold">Tire a sua idéia do papel</p>
                        <p class="text-lg font-thin mb-6">A sua nova página está á um clique de distância</p> 
                        <a 
                            href="https://wa.me/5518997648833?text=Oi!%20Estou%20interessado%20em%20seus%20servi%C3%A7os%20e%20gostaria%20de%20saber%20mais%20sobre%20isso.%20Voc%C3%AA%20poderia%20me%20enviar%20mais%20informa%C3%A7%C3%B5es?%20Obrigado!" 
                            target="_blank" rel="noopener noreferrer"
                            class="block w-full rounded-lg bg-emerald-900 px-6 pb-2 pt-2.5 text-sm font-medium uppercase leading-normal text-white shadow-primary-3 hover:bg-emerald-800"
                        >
                            Me Interesso
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex my-5 mx-5 text-white p-12 justify-center items-center bg-gradient-to-r from-slate-900 to-stone-900" ref="questions">
            <div class="md:px-12">
                <div class="divide-y divide-gray-100">
                    <details class="group" v-for="(qa) of questionsAndAnswers">
                        <summary
                            class="flex cursor-pointer list-none items-center justify-between py-4 text-lg font-medium text-secondary-900 group-open:text-primary-500">
                            {{ qa.question }}
                            <div>
                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                    stroke="currentColor" class="block h-5 w-5 group-open:hidden">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                                </svg>
                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                    stroke="currentColor" class="hidden h-5 w-5 group-open:block">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12h-15" />
                                </svg>
                            </div>
                        </summary>
                        <div class="pb-4 text-secondary-500">{{ qa.answer }}</div>
                    </details>
                </div>
            </div>
        </div>
        <div class="flex mt-5 mx-5 text-white p-12 justify-center items-center bg-neutral-900">
            <div class="px-4 pt-16 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8">
                <div class="grid gap-10 row-gap-6 mb-8 sm:grid-cols-2 lg:grid-cols-4">
                    <div class="sm:col-span-2">
                        <button @click="goTo('home')" aria-label="Go home" title="Company" class="border rounded-lg lg:border-0 inline-flex items-center">
                            <brunoPanassiIcon :size="95" />
                        </button>
                    </div>
                    <div class="space-y-2 text-sm">
                        <p class="text-base font-bold tracking-wide text-white">Contato</p>
                        <div class="flex">
                            <p class="mr-1 text-white">Telefone:</p>
                            <a href="tel:+5518997648833" aria-label="Our phone" title="Our phone" class="transition-colors duration-300 text-deep-purple-accent-400 hover:text-deep-purple-800">(18) 99764-8833</a>
                        </div>
                        <div class="flex">
                            <p class="mr-1 text-white">Email:</p>
                            <a href="mailto:bhenrique95@outlook.com" aria-label="Our email" title="Our email" class="transition-colors duration-300 text-deep-purple-accent-400 hover:text-deep-purple-800">bhenrique95@outlook.com</a>
                        </div>
                        <div class="flex">
                            <p class="mr-1 text-white">Endereço:</p>
                            <a href="https://www.google.com/maps" target="_blank" rel="noopener noreferrer" aria-label="Our address" title="Our address" class="transition-colors duration-300 text-deep-purple-accent-400 hover:text-deep-purple-800">
                            Avenida Antonio Cavasana 765, Araçatuba - SP
                            </a>
                        </div>
                    </div>
                    <div>
                        <span class="text-base font-bold tracking-wide text-white">Rede Social</span>
                        <div class="flex items-center mt-1 space-x-3">
                            <a href="/" class="text-gray-400 transition-colors duration-300 hover:text-deep-purple-accent-400">
                            <svg viewBox="0 0 30 30" fill="currentColor" class="h-6">
                                <circle cx="15" cy="15" r="4"></circle>
                                <path
                                d="M19.999,3h-10C6.14,3,3,6.141,3,10.001v10C3,23.86,6.141,27,10.001,27h10C23.86,27,27,23.859,27,19.999v-10   C27,6.14,23.859,3,19.999,3z M15,21c-3.309,0-6-2.691-6-6s2.691-6,6-6s6,2.691,6,6S18.309,21,15,21z M22,9c-0.552,0-1-0.448-1-1   c0-0.552,0.448-1,1-1s1,0.448,1,1C23,8.552,22.552,9,22,9z"
                                ></path>
                            </svg>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="flex flex-col-reverse justify-between pt-5 pb-10 border-t lg:flex-row">
                    <p class="text-sm text-gray-600">
                    © Copyright 2024 Bruno Panassi. Todos os direitos reservados.
                    </p>
                    <ul class="flex flex-col mb-3 space-y-2 lg:mb-0 sm:space-y-0 sm:space-x-5 sm:flex-row">
                    <li>
                        <button @click="goTo('questions')" class="text-sm text-gray-600 transition-colors duration-300 hover:text-deep-purple-accent-400">F.A.Q</button>
                    </li>
                    <li>
                        <button @click="goTo('home')" class="text-sm text-gray-600 transition-colors duration-300 hover:text-deep-purple-accent-400">Home</button>
                    </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import brunoPanassiIcon from "~/icons/brunoPanassiIcon.vue"

function onToggle() {
    const mobileMenu = document.getElementById('mobile-menu');
    mobileMenu?.classList.toggle('hidden');
}

const cincoPassos = ref<HTMLDivElement>();
const cta = ref<HTMLDivElement>();
const sobre = ref<HTMLDivElement>();
const home = ref<HTMLDivElement>();
const questions = ref<HTMLDivElement>();

const roofElement = ref()

const calendlyOptions = {
    url: 'https://calendly.com/bhenrique95?hide_gdpr_banner=1',
    text: "Agendar"
}

const questionsAndAnswers = [
    {
        question: "É utilizado Wordpress?",
        answer: "Não, é utilizado Nuxt para a criação de landing pages junto com o Tailwind para estilização de classes."
    },
    {
        question: "O Nuxt é bom para landing pages?",
        answer: "Sim, o Nuxt possui SSR o que facilita para a performance e também para o SEO da página."
    },
    {
        question: "Você fornece serviços de hospedagem?",
        answer: "Não, o projeto é entregue com os arquivos necessários para deploy, e é feito o encaminhamento para algum serviço de hospedagem de confiança."
    },
    {
        question: "Qual o tempo médio para a entrega de um projeto",
        answer: "Procuramos dar foco na prioridade do cliente junto com a complexidade do seu projeto, porém um tempo médio para a criação de uma landing page seria de 7 dias."
    },
    {
        question: "Qual o preço mínimo para um projeto?",
        answer: "O preço pode começar em R$800, podendo variar de acordo com a sua prioridade e complexidade."
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

const blockRefToGo = [
    {
        id: 'cinco-passos',
        block: cincoPassos
    },
    {
        id: 'cta',
        block: cta
    },
    {
        id: 'sobre',
        block: sobre
    },
    {
        id: 'home',
        block: home
    },
    {
        id: 'questions',
        block: questions
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
.body-custom {
    background-color: #0E1013;
    overflow-x: hidden;
}

.html-custom {
    overflow-x: hidden;
}
@keyframes typing {
  0.0000%, 27.3488% { content: ""; }
  1.1395%, 26.2093% { content: "o"; }
  2.2791%, 25.0698% { content: "on"; }
  3.4186%, 23.9302% { content: "ont"; }
  4.5581%, 22.7907% { content: "onte"; }
  5.6977%, 21.6512% { content: "ontem"; }

  30.7674%, 51.2791% { content: ""; }
  31.9070%, 50.1395% { content: "h"; }
  33.0465%, 49.0000% { content: "ho"; }
  34.1860%, 47.8605% { content: "hoj"; }
  35.3256%, 46.7209% { content: "hoje"; }

  54.6977%, 75.2093% { content: ""; }
  55.8372%, 74.0698% { content: "a"; }
  56.9767%, 72.9302% { content: "am"; }
  58.1163%, 71.7907% { content: "ama"; }
  59.2558%, 70.6512% { content: "aman"; }
  60.3953%, 69.5116% { content: "amanh"; }
  61.5349%, 68.3721% { content: "amanhã"; }
}

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

.typewriter {
  --caret: currentcolor;
}

.typewriter::before {
  content: "";
  animation: typing 13.5s infinite;
}

.typewriter::after {
  content: "";
  border-right: 1px solid var(--caret);
  animation: blink 0.5s linear infinite;
}

.typewriter.thick::after {
  border-right: 1ch solid var(--caret);
}

.typewriter.nocaret::after {
  border-right: 0;
}


@media (prefers-reduced-motion) {
  .typewriter::after {
    animation: none;
  }
  
  @keyframes sequencePopup {
    0%, 100% { content: "ontem"; }
    25% { content: "hoje"; }
    50% { content: "amanhã"; }
  }

  .typewriter::before {
    content: "ontem";
    animation: sequencePopup 12s linear infinite;
  }
}
</style>
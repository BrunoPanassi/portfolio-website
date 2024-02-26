<template>
    <div>
        <div class="flex h-screen justify-center items-center font-sans gradient" v-motion-slide-top :delay="500">
            <div class="text-center">
                <p class="text-3xl font-bold text-zinc-50">Bruno Panassi</p>
                <p class="text-xl font-semibold text-slate-300">Mid Full Stack Web Developer</p>
                <div class="flex justify-center space-x-5 pt-3 icon">
                    <a v-for="(link) of mainLinks"
                    :href="link.ref" target="_blank" rel="noopener noreferrer">
                        <Icon :name="link.icon"/>
                    </a>
                </div>
                <div class="mt-5">
                    <p v-for="(link) of secundaryLinks" @click="goTo(link.goTo)" class="mt-2 cursor-pointer bg-transparent text-slate-100 text-base font-mono font-semibold py-1 px-2 border border-slate-100 rounded-lg">
                        {{ link.title }}
                    </p>
                </div>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center font-sans my-5 mx-5 section" ref="aboutNowBlock" v-motion-slide-visible-once-left :delay="500">
            <div class="text-left px-10">
                <button v-for="(value, index) of aboutMeButtons" @click="selectAboutMe(index)" :class="getBackgroundOnSelectedButton(index)">
                    {{ value.text }}
                </button>
                <p class="mt-5 text-lg font-normal text-zinc-50" style="white-space: pre-wrap; line-height: 1.6;">{{ selectedParagraph }}</p>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center my-5 mx-5 section icon" ref="stacks" v-motion-slide-visible-once-right :delay="500">
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
        <div class="flex justify-center items-center my-5 mx-5 section icon px-5 py-12" ref="professionalExperience" v-motion-slide-visible-once-bottom :delay="500">
            <!-- TW Elements is free under AGPL, with commercial license required for specific uses. See more details: https://tw-elements.com/license/ and contact us for queries at tailwind@mdbootstrap.com --> 
            <ol class="border-l border-neutral-300 dark:border-neutral-500">
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
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue';

const aboutNowBlock = ref<HTMLDivElement>();
const stacks = ref<HTMLDivElement>();
const professionalExperience = ref<HTMLDivElement>();

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
        goTo: "",
        title: "PROJECTS"
    },
    {
        goTo: "",
        title: "OTHERS"
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
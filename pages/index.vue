<template>
    <div>
        <div class="flex h-screen justify-center items-center font-sans gradient" v-motion-slide-top :delay="500">
            <div class="text-center">
                <p class="text-3xl font-bold text-zinc-50">Bruno Panassi</p>
                <p class="text-xl font-semibold text-slate-300">Mid Full Stack Web Developer</p>
                <div class="flex justify-center space-x-5 pt-3 icon">
                    <MdiIcon icon="mdiLinkedin"/>
                    <MdiIcon icon="mdiGithub"/>
                    <MdiIcon icon="mdiEmail"/>
                </div>
                <div class="mt-5">
                    <p @click="goTo('about-now')" class="mt-2 cursor-pointer bg-transparent text-slate-100 text-base font-mono font-semibold py-1 px-2 border border-slate-100 rounded-lg">ABOUT</p>
                    <p @click="goTo('stacks')" class="mt-2 cursor-pointer bg-transparent text-slate-100 text-base font-mono font-semibold py-1 px-2 border border-slate-100 rounded-lg">STACKS</p>
                    <p class="mt-2 cursor-pointer bg-transparent text-slate-100 text-base font-mono font-semibold py-1 px-2 border border-slate-100 rounded-lg">PROFESSIONAL EXPERIENCE</p>
                    <p class="mt-2 cursor-pointer bg-transparent text-slate-100 text-base font-mono font-semibold py-1 px-2 border border-slate-100 rounded-lg">PROJECTS</p>
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
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiVuejs"/>
                        </div>
                        <span>Vue.js</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiVuetify"/>
                        </div>
                        <span>Vuetify</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiNuxt"/>
                        </div>
                        <span>Nuxt.js</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiLanguageTypescript"/>
                        </div>
                        <span>Typescript</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiLanguageJavascript"/>
                        </div>
                        <span>Javascript</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiLanguageJava"/>
                        </div>
                        <span>Java</span>
                    </div>
                    <div class="flex text-base space-x-2 mt-2 px-2 chip">
                        <div style="font-size: 30px">
                            <MdiIcon icon="mdiTailwind"/>
                        </div>
                        <span>Tailwind</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue';

const aboutNowBlock = ref<HTMLDivElement>();
const stacks = ref<HTMLDivElement>();

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
    height: 100vh;
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
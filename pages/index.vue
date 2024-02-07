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
            </div>
        </div>
        <div class="flex h-screen justify-center items-center font-sans my-5 mx-5 section" v-motion-slide-visible-once-left :delay="500">
            <div class="text-left px-10">
                <p class="text-lg font-semibold text-zinc-50">About Now</p>
                <p class="text-lg font-normal text-zinc-50">{{ aboutNow }}</p>
            </div>
        </div>
        <div class="flex h-screen justify-center items-center my-5 mx-5 section icon" v-motion-slide-visible-once-right :delay="500">
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
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue';

useHead({
  htmlAttrs: {
    class: 'html-custom'
  },
  bodyAttrs: {
    class: 'body-custom'
  }
})

const aboutNow = computed(() => "Creating Carofy, a project made with Nuxt.js + Vue.js + Typescript, made for content creators, to help create image carousels for instagram and linkedin.")

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
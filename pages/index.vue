<template>
    <div>
        <div class="font-sans gradient">
            <div class="flex space-x-2 pl-5 pt-5 icon">
                <MdiIcon icon="mdiLinkedin"/>
                <MdiIcon icon="mdiGithub"/>
                <MdiIcon icon="mdiEmail"/>
            </div>
            <div class="grid grid-flow-row auto-rows-max justify-items-center content-center py-16">
                <p class="text-3xl font-bold text-zinc-50">Bruno Panassi</p>
                <p class="text-xl font-semibold text-slate-300">Mid Full Stack Web Developer</p>
            </div>
        </div>
        <div class="py-5 pl-5 mt-5 section">
            <p class="text-lg font-semibold text-zinc-50">About Now</p>
            <p class="text-lg font-normal text-zinc-50">{{ aboutNow }}</p>
        </div>
        <div class="py-5 pl-5 mt-5 section icon">
            <p class="text-lg font-semibold text-zinc-50">Main Stacks</p>
            <div class="flex mt-2">
                <MdiIcon icon="mdiVuejs"/>
                <MdiIcon icon="mdiVuetify"/>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted, computed } from 'vue';

onMounted(() => {
    document.body.style.backgroundColor = '#0E1013'
})

const aboutNow = computed(() => "Creating Carofy, a project made with Nuxt.js + Vue.js + Typescript, made for content creators, to help create image carousels for instagram and linkedin.")

</script>

<style scoped>
.gradient {
	height: 300px;
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

#body {
    background-color: black;
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
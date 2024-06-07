<template>
    <svg :width="props.size" :height="props.size" viewBox="0 0 15 15">
        <path stroke="#ffffff" stroke-linejoin="round" d="m.5 12.5 6-10 6 10H.5Z"/>
        <path stroke="#ffffff" stroke-linejoin="round" d="m4.5 12.5 5-8.5 5 8.5h-10Z"/>
    </svg>
</template>

<script setup lang="ts">
const props = defineProps(['size'])
</script>

<style scoped>

</style>
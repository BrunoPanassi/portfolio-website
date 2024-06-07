<template>
  <svg :width="props.size" :height="props.size" viewBox="0 0 16 16">
    <path
      fill="#ffffff"
      d="M11.753 1h-1.336a.75.75 0 0 0-.631.344L8 4.122 6.214 1.344A.75.75 0 0 0 5.584 1H.75a.75.75 0 0 0-.647 1.13l7.25 12.351a.75.75 0 0 0 1.294 0l7.25-12.351A.75.75 0 0 0 15.25 1h-3.497ZM3.81 2.5 8 9.683 12.19 2.5h1.75L8 12.62 2.06 2.5h1.75Z"
    />
  </svg>
</template>

<script setup lang="ts">
    const props = defineProps(["size"]);
</script>

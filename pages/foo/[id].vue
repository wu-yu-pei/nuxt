<template>
  <div class="foo">{{ route.params.id }}</div>
</template>

<script setup lang="ts">
const route = useRoute();
console.log(route.params);
</script>

<style scoped></style>

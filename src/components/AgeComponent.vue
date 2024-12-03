<script setup>
 const model = defineModel()
</script>
 
<template>

<div>
    <h2 class="text-green-700">From Age Component {{ model }}</h2>
    <input type="number" v-model="model">
</div>
</template>
 
<style scoped>
 
</style>
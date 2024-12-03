<script setup>
//  defineProps(['firstName', 'lastName'])
const firstName = defineModel('firstName')
const lastName = defineModel('lastName')
</script>
 
<template>
    <h2 class="text-red-700">From Component {{ firstName }} {{ lastName }}</h2>
    <input type="text" v-model="firstName">
    <input type="text" v-model="lastName">
</template>
 
<style scoped>
 
</style>
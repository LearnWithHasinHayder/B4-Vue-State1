<script setup>
 import {inject} from 'vue'
 const theme = inject('themex')
</script>
 
<template>
    <div>

        <h1>Component - Theme Color = {{ theme.color }} <br> Text Size = {{ theme.size }} </h1>
        <input class="border border-gray-600 p-2" type="text" v-model="theme.color" placeholder="Color" />
        <input class="border border-gray-600 p-2" type="number" v-model="theme.size" placeholder="Size" />
    </div>
</template>
 
<style scoped>
 
</style>
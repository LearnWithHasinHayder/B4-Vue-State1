<script setup>
import {ref, reactive} from 'vue'
const theme = reactive({
  buttonColor:'lime',
  buttonTextSize:'43'
})
 const color=ref('lime')
 const textSize=ref('43')
</script>
 
<template>
  <button class="text-white font-bold py-2 px-4 rounded" 
  :class="`bg-${theme.buttonColor}-500 hover:bg-${theme.buttonColor}-700`"
  :style="`font-size: ${theme.buttonTextSize}px`"
  >
    Button
  </button>

  <div class="mt-20">
    <input class="border border-gray-400 p-2" type="text" v-model="theme.buttonColor" placeholder="color" />
    <input class="border border-gray-400 p-2" type="number" v-model="theme.buttonTextSize" placeholder="textSize" />
  </div>
</template>
 
<style scoped>
 
</style>
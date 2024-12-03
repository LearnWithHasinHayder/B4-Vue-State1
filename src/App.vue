<script setup>
import {reactive} from 'vue'
import { provide} from 'vue'
 import {person} from './data/person'
 import NameComponent from './components/NameComponent.vue';
 import AgeComponent from './components/AgeComponent.vue';
 import ExternalComponent from './components/ExternalComponent.vue';
 import ThemeComponent from './components/ThemeComponent.vue';

 const theme = reactive({
   color:'lime',
   size:'43'
 })

 provide('themex',theme)
</script>
 
<template>
  <div>
    <h1> Name = {{ person.firstName }} {{ person.lastName }} </h1>
    <NameComponent v-model:firstName="person.firstName" v-model:lastName="person.lastName" />
    <AgeComponent v-model="person.age" />
  </div>
  <div class="mt-10">
    <button @click="console.log(person)" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      Export
    </button>
  </div>
  <div>
    <ExternalComponent />
  </div>
  <div class="mt-10">
    <hr>
    <h1>
      Theme Color = {{ theme.color }} <br>
      Theme Size = {{ theme.size }}
    </h1>
  </div>
  <div class="mt-10">
    <hr>
    <ThemeComponent />
  </div>
</template>
 
<style scoped>
 
</style>
<script setup>
  import {ref} from 'vue'
  const firstName = ref("John")
  const lastName = ref("Doe")
  const age=ref(25)

  import NameComponent from './components/NameComponent.vue'
  import AgeComponent from './components/AgeComponent.vue'
</script>
 
<template>
  <div>
    <h1> Name = {{ firstName }} {{ lastName }} {{ age }} </h1>
    <input class="border border-gray-600 p-2" type="text" v-model="firstName" placeholder="First Name" />
    <input class="border border-gray-600 p-2" type="text" v-model="lastName" placeholder="Last Name" />
  </div>

  <div>
    <NameComponent v-model:firstName="firstName" v-model:lastName="lastName" />
  </div>
  <div>
    <AgeComponent v-model="age" />
  </div>
</template>
 
<style scoped>
 
</style>
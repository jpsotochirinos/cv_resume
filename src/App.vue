<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import SlidePart from "./components/SlidePart.vue";
import { ref } from "vue";
let slide = ref(0)
const customChange = (e)=>{
  slide.value = e
}

</script>

<template>
  <v-app>
  <div data-app id="app" >
 
        <main >
        <SlidePart />
        </main>



  </div>
</v-app>
</template>

<style scoped>

</style>

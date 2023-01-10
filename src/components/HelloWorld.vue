<script setup>
import IconTooltip from "./IconTooltip.vue";
import { ref } from "vue";

const skills = ref([
  {
    tooltip:'Python',
    imgUrl:'https://asset.brandfetch.io/idbpOFBgcc/idLAZHCBEl.png'
  },
  {
    tooltip:'JavaScript',
    imgUrl:'https://asset.brandfetch.io/idq5ck33b2/id8Fb4RR16.png'
  },
  {
    tooltip:'Vue 2 y 3',
    imgUrl:'https://asset.brandfetch.io/idT-7aLCAj/idoQBGg2PO.jpeg'
  },
  {
    tooltip:'SQL Server',
    imgUrl:'https://asset.brandfetch.io/idbpOFBgcc/idLAZHCBEl.png'
  },
  {
    tooltip:'Google Cloud Platform',
    imgUrl:'https://asset.brandfetch.io/idbpOFBgcc/idLAZHCBEl.png'
  },
  {
    tooltip:'WSL',
    imgUrl:'https://asset.brandfetch.io/idbpOFBgcc/idLAZHCBEl.png'
  },
  {
    tooltip:'Ubuntu 20.04',
    imgUrl:'https://asset.brandfetch.io/idQx9ZiJAu/idZVbuEUio.svg'
  },
])
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="flex align-self-center">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      Desarrollador Back-end y Front-end
    </h3>
    <br/>
    <div class="pa-2 align-self-start">
      <IconTooltip v-for="skill in skills" :tooltip="skill.tooltip" :imgUrl="skill.imgUrl"/>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    display: block;
    text-align: center;
  }

}
</style>

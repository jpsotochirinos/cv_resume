<script setup>
import { computed } from 'vue';

const varProps = defineProps({
  tooltip: {
    type: String
  },
  imgUrl: {
    type: String
  }
})

const urlSearch = computed(()=>new URL(varProps.imgUrl, import.meta.url).href)

</script>

<template>
  
  <v-tooltip bottom>
        <template v-slot:activator="{ on, attrs }">

                <v-list-item-avatar
                  style="margin: 10px"
                
                  size="40"
                  v-bind="attrs"
                  v-on="on"
                  >
                  
                      <img
                      :src="urlSearch"
                      >
                    
                  </v-list-item-avatar>

        </template>
        <span>{{tooltip}}</span>
      </v-tooltip>
      
</template>
<style>
img {
    position:absolute;
    top:0;
    left:0;
    -webkit-transform-origin:50% 300%!important;
    transform-origin:50% 300%!important;
    border-radius:100px;
    border-style: solid;
    border-width: 10px;
    border-color: dodgerblue;
    border: 10px;
    height:150px;
    }
</style>
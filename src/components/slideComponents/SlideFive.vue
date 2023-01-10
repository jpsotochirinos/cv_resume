<script setup>
import { ref,computed } from "vue";
const items = ref([
        {
          src: computed(()=>new URL('../../assets/imgs/03.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=lur5Xjet8QA',
          text: 'KNN’s explanation'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/04.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=YLoxkSeH-Io',
          text: 'NeRF’s explanations '
        },
        {
          src: computed(()=>new URL('../../assets/imgs/09.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=VBmQhvE9q4c&list=PLz1Ngwb5F-dX27OCkPMkLmigYX6SwCui5',
          text: 'Render Models'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/07.jpg', import.meta.url).href),
          url: 'https://play.google.com/store/apps/details?id=com.kusikuy.candelaria',
          text: 'Kusykuy Candelaria APP'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/08.jpg', import.meta.url).href),
          url: 'https://play.google.com/store/apps/details?id=com.soch.culturFest',
          text: 'CulturFest APP'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/10.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=wCQlIte1x_s&list=PLcy2pW9hRYszNHu_1BI23-wNb9Y5RoYED',
          text: 'Corporate rebranding'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/01.jpg', import.meta.url).href),
          url: 'https://youtu.be/9NAIr10t7fM',
          text: 'Covid Spot'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/02.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=sdjqugWaCgg',
          text: 'Disinfectant Spot'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/05.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=9IoW87rJ3kc',
          text: 'Disinfectant Spot'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/06.png', import.meta.url).href),
          url: 'https://www.youtube.com/watch?v=wCQlIte1x_s&list=PLcy2pW9hRYszNHu_1BI23-wNb9Y5RoYED',
          text: 'Informative career videos'
        },
        {
          src: computed(()=>new URL('../../assets/imgs/11.png', import.meta.url).href),
          url: 'https://youtu.be/a-4sM9im2cg',
          text: '3D printers Video'
        },
        
      ])
let selected = ref([])
const icon  = computed(()=>new URL('../../assets/sgvs/link.svg', import.meta.url).href)
const img =  (e)=>new URL(e, import.meta.url).href
const gohref = (e) =>{
      window.open(e);
}
 
</script>


<template>

        <v-card 
            dark
            tile
            max-height="1240px"
            height="929px"
            min-width="400"
            
        >
        <v-container>
        <v-row justify="space-around">

            <v-img
            height="150px"
            src="https://cdn.pixabay.com/photo/2018/03/13/02/43/eye-3221498_1280.jpg"
            >
            <v-card-title style="font-size: 3rem;padding: 50px;">Designs</v-card-title>
            </v-img>

            <div class="scroll4">
                <v-item-group
                    v-model="selected"
                    multiple
                >
                <v-row>
                <v-col
                    v-for="(item, i) in items"
                    :key="i"
                    cols="12"
                    md="6"
                >
                    <v-item v-slot="{ active, toggle }">
                    <v-card>
                    <v-img
                        :src="item.src"
                        height="200"
                        class="text-right pa-2"
                        @click="toggle"
                    >
                        
                        <v-btn
                        fab
                        small
                        @click="gohref(item.url)"
                        >
                        
                        <img
                          style="height:32px ;width: 32px; margin-top: -15px;margin-left: 4px;"
                          :src="icon"
                          >
                        </v-btn>
                      
                    </v-img>
                    <v-card-title class="text-h6">
                      {{item.text}}
                    </v-card-title>
                  </v-card>
                    </v-item>
                    
                </v-col>
                </v-row>
      </v-item-group>
            </div>
        
            
    

            

        </v-row>
    </v-container>
    </v-card>

</template>
<style>
div.scroll4 {
  width: 1000px;
  height: 780px;
  margin-top: 30px;
  overflow-x: hidden;
  overflow-y: auto;
  
}
div.scroll4::-webkit-scrollbar{
    display: none;
}
.avatar{
    margin-left: -35px;
    margin-bottom: 7px;
}
.timeline{
    margin: 15px;
}
</style>
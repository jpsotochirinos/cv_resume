<script setup>
import { computed,ref } from "vue";

const years = ref([
        {
          color: 'white',
          year: 'Publications',
          projects: [{
          job:'Neural Rendering in the Cloud with Tensor Processing Unit - ICMECE 2022 Barcelona conference Octobre 2022',
          text: 'A scalable cloud-based Neural Rendering Prototype System (NRPS) implemented in Python, testing 3 designed architectures: (1) TPU VM, (2) TPU Node, (3) TPU Node with GKE.',
          url:'http://icmece.org/2022/programme2022_O.pdf',
            }
        ]
          
        },
        {
          color: 'white',
          year: 'Presentations',
          projects: [{
                job:'Neural Rendering in the Cloud with Tensor Processing Unit - ICMECE 2022 Barcelona conference  Octobre 2022',
                text: 'A scalable cloud-based Neural Rendering Prototype System (NRPS) implemented in Python, testing 3 designed architectures: (1) TPU VM, (2) TPU Node, (3) TPU Node with GKE.',
                url:'http://icmece.org/2022/programme2022_O.pdf',
            },
            {
                job:'INTRODUCTION TO THE USE OF CLOUD TPU RESOURCES IN GOOGLE KUBERNETES ENGINE FOR NOVEL VIEW SYNTHESIS December 2021',
                text: 'This paper explores Novel View Synthesis as an alternative for sustainable digitization by applying a Neural Radiation Field network implemented in JAX for the development of a Prototype Neural Rendering System.',
                url:'https://fb.watch/hVNJ4_HY8n/'
            },
        ]
          
        }
      ])
const github = computed(()=>new URL('../../assets/sgvs/link.svg', import.meta.url).href)
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
            src="https://cdn.pixabay.com/photo/2017/09/08/20/29/chess-2730034_1280.jpg"
            >
            <v-card-title style="font-size: 3rem;padding: 50px;">Publications</v-card-title>
            </v-img>


            <div class="scroll3">
                
                
                <v-timeline
                :reverse="false"
                dense
                >
                <v-timeline-item
                v-for="(year, i) in years"
                :key="i"
                :color="year.color"
                dark
                hide-dot
                class="timeline"
                >


                <v-avatar
                color="white"
                size="15"
                class="avatar"
                ></v-avatar>
                <span
                :class="`headline font-weight-bold ${year.color}--text`"
                style="margin-left: 10px;"
                v-text="year.year"
                ></span>
                <div v-for="project in year.projects">
                <div class="py-4">
                    
                    <h2 :class="`headline font-weight-light mb-2 ${year.color}--text`">
                    {{ project.title }}
                    </h2>
                    <h2 class="  mb-1 ">
                    {{ project.job }}
                    </h2>
                    <div>
                    {{ project.text }}
                    </div>
                </div>
                <div >
                        <v-chip
                        v-for="(tag,i) in project.tags"
                        class="ma-2"
                        :color="tag.color"
                        >
                        {{tag.name}}
                        </v-chip>
                        <v-btn
                          class="mx-1"
                          fab
                          small
                          color="black"
                          depressed
                          @click="gohref(project.url)"
                          >
                          <img
                          style="height:32px ;width: 32px; margin-top: -15px;margin-left: 4px;"
                          :src="github"
                          >
                          </v-btn>
                </div>
                
                </div>
                </v-timeline-item>
            </v-timeline>
            
            </div>
        
            
    

            

        </v-row>
    </v-container>
    </v-card>

</template>
<style>
div.scroll3 {
  width: auto;
  height: 780px;
  overflow-x: hidden;
  overflow-y: auto;
  
}
div.scroll3::-webkit-scrollbar{
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
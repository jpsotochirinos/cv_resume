<script setup>
import { ref,computed } from "vue";

const years = ref([
        {
          color: 'white',
          year: 'Master Degree Proyects',
          projects: [{
          job:'Data Structure',
          text: 'A brief review of the most popular search algorithms. Implementation of data structures: Binary trees, AVL, QuadTree, Octree and KD Tree. Implementation of the KNN algorithm.',
          url:'https://github.com/jpsotochirinos/data_structure_examples',
          tags:[
            {
                name: 'C++',
                color: 'blue darken-4'
            },
            {
                name: 'JavaScript',
                color: 'lime'
            },

          ]
        },
        {
          job:'Detection of Minerals and bases in StarCraft',
          text: 'Implementation of the RCNN algorithm in Python and Jupyternotebooks trained with a proprietary dataset generated from Inkscape.',
          url:'https://github.com/jpsotochirinos/SC_detection',
          tags:[
            {
                name: 'Python',
                color: 'blue lighten-1'
            },
            {
                name: 'Jupyter Notebook',
                color: 'orange'
            },


          ]
        },
        {
          job:'Cloud Computing and DataBases',
          text: 'Python implementation of inverted index for large texts.',
          url:'https://github.com/jpsotochirinos/data_structure_examples',
          tags:[
            {
                name: 'Python',
                color: 'blue lighten-1'
            },

          ]
        },
        {
          job:'AI Examples',
          text: 'Understand the use and performance of Linear Regression, Logistic Regression, Downward Gradient Algorithm, RNN and genetic algorithms, testing with outlier and normal sets to understand the scope of each method and its performance.',
          url:'https://github.com/jpsotochirinos/data_structure_examples',
          tags:[
            {
                name: 'Python',
                color: 'blue lighten-1'
            }
          ]
        },
        ]
          
        },
        {
          color: 'white',
          year: 'Personal Proyects',
          projects: [{
          job:'KDTree work with JAX in TPU resource',
          text: 'An implementation of kdtree and knn using Numpy and JAX in TPU VM testing Movie Lens Data Base.',
          url:'https://github.com/jpsotochirinos/KNN_TPU',
          tags:[
            {
                name: 'Python',
                color: 'blue darken-4'
            }
          ]
        },
        {
          job:'Prototype Neural Rendering System using JAXNERF in the Cloud',
          text: 'A scalable cloud-based Neural Rendering Prototype System (NRPS) implemented in Python, testing 3 designed architectures: (1) TPU VM, (2) TPU Node, (3) TPU Node with GKE.',
          url:'https://github.com/jpsotochirinos/jaxnerf',
          tags:[
            {
                name: 'Python',
                color: 'blue lighten-1'
            },
            {
                name: 'Google Cloud Platform',
                color: 'light-blue accent-2'
            },
            {
                name: 'Kubernetes',
                color: 'light-blue'
            },
            {
                name: 'Docker',
                color: 'blue darken-4'
            },
            {
                name: 'NeRF',
                color: 'grey '
            },

          ]
        }
        ]
          
        }
      ])
const github = computed(()=>new URL('../../assets/sgvs/github.svg', import.meta.url).href)
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
            src="https://cdn.pixabay.com/photo/2017/02/08/12/46/moon-2048727_1280.jpg"
            >
            <v-card-title style="font-size: 3rem;padding: 50px;">Projects</v-card-title>
            </v-img>


            <div class="scroll2">
                
                
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
div.scroll2 {
  width: auto;
  height: 780px;
  overflow-x: hidden;
  overflow-y: auto;
  
}
div.scroll2::-webkit-scrollbar{
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
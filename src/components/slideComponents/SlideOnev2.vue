<script setup>
import { ref, computed } from "vue";
const likedin = computed(()=>new URL('../../assets/sgvs/linkedin.svg', import.meta.url).href)
const github = computed(()=>new URL('../../assets/sgvs/github.svg', import.meta.url).href)
const fb = computed(()=>new URL('../../assets/sgvs/fb.svg', import.meta.url).href)
const urlSearch = (e)=>new URL(e, import.meta.url).href
const skills = ref([
  {
    tooltip:'Python',
    imgUrl:computed(()=>new URL('../../assets/sgvs/python_icon.svg', import.meta.url).href)
  },
  {
    tooltip:'JavaScript',
    imgUrl:computed(()=>new URL('../../assets/sgvs/js_icon.svg', import.meta.url).href)
  },
  {
    tooltip:'Vue',
    imgUrl:computed(()=>new URL('../../assets/sgvs/vue_icon.svg', import.meta.url).href)
  },
   {
    tooltip:'Google Cloud Platform',
    imgUrl:computed(()=>new URL('../../assets/sgvs/gcp.svg', import.meta.url).href)
  },
  {
    tooltip:'WSL',
    imgUrl:computed(()=>new URL('../../assets/sgvs/wsl.svg', import.meta.url).href)
  },
  {
    tooltip:'Ubuntu 20.04',
    imgUrl:computed(()=>new URL('../../assets/sgvs/ubuntu-icon.svg', import.meta.url).href)
  },
])
const soft_skill = ref([
  {
    tooltip:'Research',
    imgUrl:computed(()=>new URL('../../assets/sgvs/curioso.svg', import.meta.url).href)
  },
  {
    tooltip:'Integrity and ethics',
    imgUrl:computed(()=>new URL('../../assets/sgvs/ethic.svg', import.meta.url).href)
  },
  {
    tooltip:'Teamwork',
    imgUrl:computed(()=>new URL('../../assets/sgvs/groupwork.svg', import.meta.url).href)
  },
   {
    tooltip:'Innovator',
    imgUrl:computed(()=>new URL('../../assets/sgvs/innovator.svg', import.meta.url).href)
  },
  {
    tooltip:'Self-taught',
    imgUrl:computed(()=>new URL('../../assets/sgvs/learn.svg', import.meta.url).href)
  },
  {
    tooltip:'Proactive',
    imgUrl:computed(()=>new URL('../../assets/sgvs/proactive.svg', import.meta.url).href)
  },
])
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
            src="https://cdn.pixabay.com/photo/2016/03/04/19/36/gears-1236578_960_720.jpg"
            >
            <v-card-title style="font-size: 3rem;padding: 50px;">About Me</v-card-title>
            </v-img>
            <div class="scroll0" >
                <v-item-group
                    style="top: 20px; "
                >
                    <div class="princ">
                    <v-img 
                      class="imgProf1"
                      style="align-self: center"
                      src="https://scontent.faqp1-1.fna.fbcdn.net/v/t1.6435-9/48382893_2208496709170571_2201053825895235584_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=174925&_nc_eui2=AeH0t5YXsxriBO3kzAaHfy73IjbWQAd6LvYiNtZAB3ou9lyxolvpsh1zdsd9vSzuIJEnNMkvNtJAhjsaeWFzu5fT&_nc_ohc=713P1L1mNUwAX8uM_iG&tn=pQmGgpTQPDMDB0ZQ&_nc_ht=scontent.faqp1-1.fna&oh=00_AfD8BtKB3_3K_sg2AlBp6ZQU8mYN88jWN34DfasWlZvQMQ&oe=63E2D2B4"
                      height="200"
                      width="200"
                      >
                      </v-img>
                    <v-card-title style="font-size: 2rem">Jean Pierre Soto Chirinos</v-card-title>    
                    <v-card-text>
                        <v-btn
                        class="mx-1"
                        fab
                        size="52px"
                        color="blue darken-4"
                        depressed
                        @click="gohref('https://www.linkedin.com/in/jean-pierre-soto-chirinos-91056222b/')"
                        >
                        <img
                        class="socialM"
                        :src="likedin"
                        >
                        </v-btn>
                        <v-btn
                        class="mx-1"
                        fab
                        size="52px"
                        color="light-blue darken-2"
                        depressed
                        @click="gohref('https://www.facebook.com/jpsotochirinosJP')"
                        >
                        <img
                        class="socialM"
                        :src="fb"
                        >
                        </v-btn>
                        <v-btn
                        class="mx-1"
                        fab
                        size="52px"
                        color="black"
                        depressed
                        @click="gohref('https://github.com/jpsotochirinos')"
                        >
                        <img
                        class="socialM"
                        :src="github"
                        >
                        </v-btn>
                    </v-card-text>
                    <div class="pa-2 align-self-start">
                        <v-card-title>Back-End & Front-End Developer</v-card-title>
                        <v-card-text>
                        <ul>
                        <li>👋 Hi, I’m Jean Pierre Soto Chirinos.</li>
                        <li>👀 I’m interested in artificial vision.</li>
                        <li>🌱 I’m currently learning a master's degree in computer science.</li>
                        <li>💡 I’m looking to collaborate on neural digitalization.</li>
                        <li>💞️ I love to design and make short animations.</li>
                        <li>🦾 I’m learning about 3D printing and robotic applications.</li>
                        <li>📫 How to reach me jsotochir@unsa.edu.pe</li>
                        </ul>
                        </v-card-text>
                    </div>
                            
                            <div class="pa-2 align-self-start" >
                                <v-card-title>My Skills</v-card-title>
                                <v-card-text>
                                    <v-tooltip v-for="skill in skills" bottom>
                                        <template v-slot:activator="{ on, attrs }">

                                                <v-list-item-avatar
                                                style="margin: 10px"
                                                
                                                size="72"
                                                v-bind="attrs"
                                                v-on="on"
                                                >
                                                
                                                    <img
                                                    :src="skill.imgUrl"
                                                    >
                                                    
                                                </v-list-item-avatar>

                                        </template>
                                        <span>{{skill.tooltip}}</span>
                                    </v-tooltip>
                                </v-card-text>    
                                </div>
                            
                            <div class="pa-2 align-self-start ">
                                <v-card-title  >My soft-skills</v-card-title>
                                <v-card-text>
                                    <v-tooltip v-for="skill in soft_skill" bottom>
                                        <template v-slot:activator="{ on, attrs }">

                                                <v-list-item-avatar
                                                style="margin: 10px"
                                                
                                                size="72"
                                                v-bind="attrs"
                                                v-on="on"
                                                >
                                                
                                                    <img
                                                    :src="skill.imgUrl"
                                                    >
                                                    
                                                </v-list-item-avatar>

                                        </template>
                                        <span>{{skill.tooltip}}</span>
                                    </v-tooltip>
                                </v-card-text>
                                </div>
                            </div>
                </v-item-group>                         
             </div>
                      

        </v-row>
    </v-container>
    </v-card>

</template>

<style >
div.scroll0 {
  width: 1000px;
  height: 780px ;
  overflow-x: hidden;
  overflow-y: auto;
}
div.scroll0::-webkit-scrollbar{
    display: none;
}

.imgProf1{
  border-radius: 100%;
}


</style>
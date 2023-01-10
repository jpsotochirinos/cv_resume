<script>
export default {
    data: () => ({
      years: [
        {
          color: 'white',
          year: 'July 2017 - December 2017',
          title: 'CCA - UNAP',
          job:'Trainee Developer',
          text: 'Experience in developing and implementing: A system for recording material assets developed in MEANS, an FTP server in FileZilla multimedia. Creation and production of multimedia content, streams, and advertising. Management of social networks with automatic tools.',
          tags:[
            {
                name: 'JavaScript',
                color: 'yellow'
            },
            {
                name: 'FileZilla',
                color: 'red'
            },
            {
                name: 'Multimedia Producction',
                color: 'blue'
            },

          ]
        },
        {
          color: 'white',
          year: 'Agust 2018 - October 2018',
          title: 'BSGrupo',
          job:'Developer Jr.',
          text: 'Experience in the development and maintenance of a modular system using PHP, KendoJS, and SQLServer. Development of new modules for accounting and marketing areas. Optimization of triggers and DB views in SQLServer. Development of a system for collecting and transforming random audios from call reports in DebianOS with SoX, performing a transcription with Azure Speech to Text service matching the information with DB in SQL Server for encapsulation of information from users with a high probability of purchase.',
          tags:[
            {
                name: 'PHP',
                color: 'light-blue darken-4'
            },
            {
                name: 'JavaSript',
                color: 'lime'
            },
            {
                name: 'Debian Os',
                color: 'red darken-3'
            },
            {
                name: 'Azure',
                color: 'blue lighten-1'
            },
            {
                name: 'SQL Server',
                color: 'indigo darken-4'
            },

          ]
        },
        {
          color: 'white',
          year: 'February 2019 & February 2020',
          title: 'KusyKuy Candelaria APP',
          job:'Back-End & Front-End Developer',
          text: 'Experience in the development and implementation of a modular system using LoopBack 2.x, Vue, Firebase, Storage, and Android. Deployment on Google Cloud Platform using Storage and Firebase services. Back-End API/REST Developed with LoopBack 2.x, MongoDB, and plugins for Storage and Firebase services for data entry, modification, deletion, multimedia, and streamings. Front-End Developer in Vue 2 using axis, routes, and Vuesax.',
          tags:[
            {
                name: 'Vue',
                color: 'green lighten-1'
            },
            {
                name: 'JavaSript',
                color: 'lime'
            },
            {
                name: 'Google Cloud Platform',
                color: 'light-blue accent-2'
            },
            {
                name: 'Firebase',
                color: 'deep-orange'
            },
            {
                name: 'Mongo DB',
                color: 'green darken-4'
            },

          ]
        },
        {
          color: 'white',
          year: 'March 2020 - Agust 2022',
          title: 'SOCH S.R.L.',
          job:'Chief Operating Officer',
          text: 'Brand development and redesign of the business concept, management, and logistics of equipment, supplies, and employees. Creation of multimedia content for social networks with Inkscape, Adobe Illustrator, and AfterEffects. Website maintenance with WordPress and brand management in social networks. Development and implementation of a report-generating system in word, excel, and pdf with Carbone, Vue, Vuesax, and Mongo DB.',
          tags:[
            {
                name: 'Vue',
                color: 'green lighten-1'
            },
            {
                name: 'JavaSript',
                color: 'lime'
            },
            {
                name: 'Mongo DB',
                color: 'green darken-4'
            },
            {
                name: 'Inkscape',
                color: 'grey darken-4'
            },
            {
                name: 'Adobe Ilustrator',
                color: 'orange darken-1'
            },
            {
                name: 'AfterEffects',
                color: 'deep-purple darken-2'
            },

          ]
        }
      ],
    }),

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
            src="https://cdn.pixabay.com/photo/2022/12/05/20/46/christmas-star-7637681_1280.jpg"
            >
            <v-card-title style="font-size: 3rem;padding: 50px;">Experience</v-card-title>
            </v-img>


            <div class="scroll1">
                
                
                <v-timeline>
                <v-timeline-item
                v-for="(year, i) in years"
                :key="i"
                color="year.color"
                dark
                hide-dot
                class="timeline"
                >


                <template v-slot:opposite>
                    <v-avatar
                    color='yellow'
                    size="15"
                    class="avatar"
                    ></v-avatar>
                    <span
                    :class="`headline font-weight-bold ${year.color}--text`"
                    v-text="year.year"
                    ></span>

                </template>
                <div class="py-4">
                    <h2 :class="`headline font-weight-light mb-2 ${year.color}--text`">
                    {{ year.title }}
                    </h2>
                    <h5 class="  mb-1 ">
                    {{ year.job }}
                    </h5>
                    <div>
                    {{ year.text }}
                    </div>
                    <div class="text-center">
                        <v-chip
                        v-for="(tag,i) in year.tags"
                        class="ma-2"
                        :color="tag.color"
                        >
                        {{tag.name}}
                        </v-chip>

                    </div>
                </div>
                </v-timeline-item>
            </v-timeline>
            
            </div>
        
            
    

            

        </v-row>
    </v-container>
    </v-card>

</template>

<style >
div.scroll1 {
  width: auto;
  height: 780px ;
  overflow-x: hidden;
  overflow-y: auto;
  text-align: center;
}
div.scroll1::-webkit-scrollbar{
    display: none;
}
.avatar{
    margin-right: 5px;
    margin-bottom: 5px;
}
.timeline{
    margin: 15px;
}
</style>
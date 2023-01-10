<script setup>

import { ref,computed } from "vue";
import { KinesisContainer, KinesisElement, KinesisDistance} from "vue-kinesis"
import SimpleName from "./name/simplename.vue";
import SlideZero from "./slideComponents/SlideZero.vue";
import SlideOne from "./slideComponents/SlideOne.vue";
import SlideOnev2 from "./slideComponents/SlideOnev2.vue";
import SlideTwo from "./slideComponents/SlideTwo.vue";
import SlideThree from "./slideComponents/SlideThree.vue";
import SlideFour from "./slideComponents/SlideFour.vue";
import SlideFive from "./slideComponents/SlideFive.vue";

      
 

</script>
<template>
    

            <v-window
                class="elevation-1"
                vertical
                show-arrows
            >
            <template class="prev" v-slot:prev="{ on, attrs }">
            <v-btn
                fab
                small
                depressed
                dark
                color="blue-grey darken-4"
                v-bind="attrs"
                v-on="on"
                
            >⬅</v-btn>
            </template>
            <template v-slot:next="{ on, attrs }">
            <v-btn
                fab
                small
                dark
                color="blue-grey darken-4"
                v-bind="attrs"
                v-on="on"
                class="next"
            >➡</v-btn>
            </template>
                <v-window-item :value="0">
                    <SlideZero/>
                </v-window-item>
                <v-window-item :value="1">
                    <SlideOnev2/>
                </v-window-item>
                <v-window-item :value="2">
                  <SlideTwo/>
                    
                </v-window-item>
                <v-window-item :value="3">
                 <SlideThree/>
                </v-window-item>
                <v-window-item :value="4">
                <SlideFour/>
                </v-window-item>
                <v-window-item :value="5">
                    <SlideFive/>
                </v-window-item>

            </v-window>




</template>
<style>



</style>
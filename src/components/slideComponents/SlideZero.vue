<script setup>
import { KinesisContainer, KinesisElement} from "vue-kinesis"
import SimpleName from "../name/simplename.vue";
import IconTooltip from "../IconTooltip.vue";
import { ref } from "vue";


</script>
<template>

        <v-card 
            dark
            tile
            max-height="1240px"
            height="929px"
            min-height="600px"
            min-width="400"
            
        >
        <div style="top: 40px; height:200px;  width: 150px;text-align:center;margin:auto;">
            <kinesis-container >
                <kinesis-element
                :strength="2"
                type="depth">
                    <kinesis-container >
                    <kinesis-element 
                        tag="img"
                        class="profs zero"
                        src="https://scontent.faqp1-1.fna.fbcdn.net/v/t39.30808-6/217864125_4505425732810979_2613852055651563826_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=174925&_nc_eui2=AeHkofDgGAoWrHZSeNrI08K_pBw2-tHlICmkHDb60eUgKXsE6UOIt_EyXZOd5Yw3EkiFSTx5LXufpjqUNdpvpriU&_nc_ohc=jSH99a_gNasAX-ylMP8&_nc_ht=scontent.faqp1-1.fna&oh=00_AfC4ONRcJhOk5JMZxDbJvTJ40jCGXMDYbKTgWR5jb_-zYg&oe=63BC672A"
                        :strength="30"
                        type="depth"
                        :maxX="13"
                        :maxY="13"
                        :minX="-13"
                        :minY="-13"
                        axis="x"
                        transformOrigin="0% 0%" />
                    </kinesis-container>
                    <SimpleName class="Sname"/>
                </kinesis-element>
            </kinesis-container>
            
        </div>
        <div class="titleback">
            <v-card-text class="text-h5 font-weight-bold">
                <h6 style="font-size: 1.5rem;">
                    Back-End & Front-End Dev
                </h6>
            </v-card-text>
            <div div class="icondevs-container">
                <kinesis-container class="kc">
                    
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/vue_icon.svg')"
                        :strength="10"
                        type="rotate"
                        axis="x"
                        :maxX="6"
                        :maxY="6"
                        :minX="-6"
                        :minY="-6"
                        transformOrigin="center center" />
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/gcp.svg')"
                        :strength="-10"
                        type="rotate"
                        axis="x"
                        :maxX="6"
                        :maxY="6"
                        :minX="-6"
                        :minY="-6"
                        transformOrigin="center center" />
                    
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/js_icon.svg')"
                        :strength="20"
                        type="rotate"
                        axis="x"
                        :maxX="11.5"
                        :maxY="11.5"
                        :minX="-11.5"
                        :minY="-11.5"
                        transformOrigin="center center" />
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/python_icon.svg')"
                        :strength="-20"
                        type="rotate"
                        axis="x"
                        :maxX="11.5"
                        :maxY="11.5"
                        :minX="-11.5"
                        :minY="-11.5"
                        transformOrigin="center center" />
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/ubuntu-icon.svg')"
                        :strength="30"
                        type="rotate"
                        axis="x"
                        :maxX="17"
                        :maxY="17"
                        :minX="-17"
                        :minY="-17"
                        transformOrigin="center center" />
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/wsl.svg')"
                        :strength="-30"
                        type="rotate"
                        axis="x"
                        :maxX="17"
                        :maxY="17"
                        :minX="-17"
                        :minY="-17"
                        transformOrigin="center center" />
                    <kinesis-element 
                        class="icondevs"
                        tag="img"
                        :src="require('../../assets/sgvs/myskills.svg')"
                        :strength="1"
                        type="depth"
                        :maxX="13"
                        :maxY="13"
                        :minX="-13"
                        :minY="-13"
                        axis="x"
                        transformOrigin="0% 0%" />
                    </kinesis-container>
            </div>
            <div class="footer">
                <kinesis-container class="kc">
                    <kinesis-element
                        :strength="10"
                        type="depth"
                    >
                       <p style="font-size: x-small;"> Designed by <a href="https://www.facebook.com/">Jean Soto</a> 💖 | 2023</p>
                    </kinesis-element>
                </kinesis-container>
            </div>

        </div>
    </v-card>

</template>

<style>
img.zero {
    position:absolute;
    top:0;
    left:0px;
    -webkit-transform-origin:50% 200%!important;
    transform-origin:50% 200%!important;
    border-radius:200px;
    height:150px;
    object-fit: fill;
    }
.prof{
    left: -60px;
}
.img-container{
    position:relative;
    width:200px;
    margin:auto;
    text-align:center}
.icondevs-container{
    width: 70px;  
    height: 70px;
    
    text-align:center;
    margin:auto;
}
.icondevs{
    -webkit-transform-origin:50% 500%!important;
    transform-origin:50% 500%!important;
    height: 72px;
}
.kc{
    top: 2rem;
}
.Sname{
        margin-top: 100%;
        margin-left: -85%;
        height: 90px;
    }
.titleback{
    top: 90px;text-align:center;margin:auto;
}
.footer{
    top: 90px;text-align:center;margin:auto;
}
@media  (min-width: 80rem){
    img.zero {
    position:absolute;
    top:0;
    left:-55px;
    -webkit-transform-origin:50% 200%!important;
    transform-origin:50% 200%!important;
    border-radius:200px;
    height:250px;
    object-fit: fill;
    }
    .footer{
        top: 300px;text-align:center;margin:auto;
    }
    .Sname{
        margin-top: 130%;
        margin-left: -75%;
        height: 200px;

    }
    .titleback{
        top: 200px;text-align:center;margin:auto;
    }
    .icondevs{
    -webkit-transform-origin:50% 500%!important;
    transform-origin:50% 500%!important;
    height: 150px;
    left: -40px;
    }

}
</style>
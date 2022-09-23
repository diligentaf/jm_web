<template>
  <div id="download" class="section"> 
    <v-container fluid>
      <h1>Products</h1><br />
      <vueper-slides lazy lazy-load-on-drag
        class="no-shadow"
        fixed-height="90%"
        :visible-slides="1"
        :slide-ratio="1 / 4"
        :dragging-distance="70"
        :arrows-outside="false"
        :touchable="true">
        <vueper-slide v-for="i in 1" :key="i" 
        :title="i.toString()"
        
        >
        <!-- + ['#ff5252', '#42b983'][i % 2] -->
          <template #content>
            <v-hover v-slot:default="{hover}">
              <v-card class="pa-md-4 mx-lg-auto text-center rounded-lg"
                max-width="500px"
                outlined rounded 
                color="#008B8B" raised shaped
                :elevation="hover ? 20 : 20"
                :class="{ up: hover }"
                >
                
                  <i class="icon icon-check"></i>
                  <v-img src="@/assets/img/evridge.png" class="d-block ml-auto mr-auto" max-width="300px" />
                    <h1 class="font-weight-heavy display-2 mb-2">{{products[i-1].title}}</h1>
                    <h1 class="font-weight-light">
                    {{products[i-1].text}}
                    </h1>
                    <v-btn rounded outlined href="https://evridge.app/" target="_blank" large
                    color="white" class="mt-4">
  
                    Visit App
                    </v-btn>
                    <div class="video d-flex align-center py-4">
                        <a @click.stop="dialog = true" class="playBut">
                          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                            xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/" x="0px" y="0px" width="60px"
                            height="60px" viewBox="0 0 213.7 213.7" enable-background="new 0 0 213.7 213.7"
                            xml:space="preserve">
                            <polygon class="triangle" id="XMLID_18_" fill="none" stroke-width="7" stroke-linecap="round"
                              stroke-linejoin="round" stroke-miterlimit="10" points="73.5,62.5 148.5,105.8 73.5,149.1 " />
      
                            <circle class="circle" id="XMLID_17_" fill="none" stroke-width="7" stroke-linecap="round"
                              stroke-linejoin="round" stroke-miterlimit="10" cx="106.8" cy="106.8" r="103.3" />
                          </svg>
                        </a>
                        <p class="subheading ml-2 mb-0">Click to watch</p>
                      </div>
                      <v-dialog v-model="dialog" max-width="640px">
                        <v-card>
                          <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
                        </v-card>
                      </v-dialog>
                </v-card>
            </v-hover>
          
           </template>  
        </vueper-slide> 
      </vueper-slides>

    
<!-- 
      <vueper-slides 3d fixed-height="300px" arrows-outside bullets-outside>
        <vueper-slide v-for="i in 9" :key="i" :title="i.toString()" />
      </vueper-slides> -->
<!--     
      <v-row align="center" justify="center">
        <v-col cols="10">
          <h1 class="products">Products</h1>
          <v-row align="center" justify="center">
            <v-col cols="12" sm="2" class="white--text text-left">
              <v-img src="@/assets/img/evridge.png" class="d-block ml-auto mr-auto" max-width="350px" />
              <h1 class="font-weight-light display-2 mb-2">Evridge</h1>
              <h1 class="font-weight-light">
                설명 써주세요
              </h1>
              <v-btn rounded outlined href="https://evridge.app/" target="_blank" large
              color="white" class="mt-4">
              <v-icon class="mr-2">
                mdi-github
              </v-icon>
              Visit App
              </v-btn>
                <div class="video d-flex align-center py-4">
                  <a @click.stop="dialog = true" class="playBut">
                    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                      xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/" x="0px" y="0px" width="60px"
                      height="60px" viewBox="0 0 213.7 213.7" enable-background="new 0 0 213.7 213.7"
                      xml:space="preserve">
                      <polygon class="triangle" id="XMLID_18_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" points="73.5,62.5 148.5,105.8 73.5,149.1 " />

                      <circle class="circle" id="XMLID_17_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" cx="106.8" cy="106.8" r="103.3" />
                    </svg>
                  </a>
                  <p class="subheading ml-2 mb-0">Click to watch</p>
                </div>
                <v-dialog v-model="dialog" max-width="640px">
                  <v-card>
                    <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
                  </v-card>
                </v-dialog>
            </v-col>


            <v-col cols="12" sm="2" class="white--text text-left">
             <v-img src="@/assets/img/evridge.png" class="d-block ml-auto mr-auto" max-width="350px" />
              <h1 class="font-weight-light display-2 mb-2">Evridge</h1>
              <h1 class="font-weight-light">
                설명 써주세요
              </h1>
              <v-btn rounded outlined href="https://evridge.app/" target="_blank" large
              color="white" class="mt-4">
              <v-icon class="mr-2">
                mdi-github
              </v-icon>
              Visit App
              </v-btn>
                <div class="video d-flex align-center py-4">
                  <a @click.stop="dialog = true" class="playBut">
                    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                      xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/" x="0px" y="0px" width="60px"
                      height="60px" viewBox="0 0 213.7 213.7" enable-background="new 0 0 213.7 213.7"
                      xml:space="preserve">
                      <polygon class="triangle" id="XMLID_18_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" points="73.5,62.5 148.5,105.8 73.5,149.1 " />

                      <circle class="circle" id="XMLID_17_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" cx="106.8" cy="106.8" r="103.3" />
                    </svg>
                  </a>
                  <p class="subheading ml-2 mb-0">Click to watch</p>
                </div>
                <v-dialog v-model="dialog" max-width="640px">
                  <v-card>
                    <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
                  </v-card>
                </v-dialog>
            </v-col>

            <v-col cols="12" sm="2" class="white--text text-left">
              <v-img src="@/assets/img/evridge.png" class="d-block ml-auto mr-auto" max-width="350px" />
               <h1 class="font-weight-light display-2 mb-2">Evridge</h1>
               <h1 class="font-weight-light">
                 설명 써주세요
               </h1>
               <v-btn rounded outlined href="https://evridge.app/" target="_blank" large
               color="white" class="mt-4">
               <v-icon class="mr-2">
                 mdi-github
               </v-icon>
               Visit App
               </v-btn>
                 <div class="video d-flex align-center py-4">
                   <a @click.stop="dialog = true" class="playBut">
                     <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                       xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/" x="0px" y="0px" width="60px"
                       height="60px" viewBox="0 0 213.7 213.7" enable-background="new 0 0 213.7 213.7"
                       xml:space="preserve">
                       <polygon class="triangle" id="XMLID_18_" fill="none" stroke-width="7" stroke-linecap="round"
                         stroke-linejoin="round" stroke-miterlimit="10" points="73.5,62.5 148.5,105.8 73.5,149.1 " />
 
                       <circle class="circle" id="XMLID_17_" fill="none" stroke-width="7" stroke-linecap="round"
                         stroke-linejoin="round" stroke-miterlimit="10" cx="106.8" cy="106.8" r="103.3" />
                     </svg>
                   </a>
                   <p class="subheading ml-2 mb-0">Click to watch</p>
                 </div>
                 <v-dialog v-model="dialog" max-width="640px">
                   <v-card>
                     <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
                   </v-card>
                 </v-dialog>
             </v-col>
            </v-row>
        </v-col>
      </v-row> -->


    </v-container>
  </div>
</template>

<script>
  import { VueperSlides, VueperSlide } from 'vueperslides'
  import 'vueperslides/dist/vueperslides.css'

  export default {
    components: {
      VueperSlides
      , VueperSlide
      ,slides: [
        {
          title: 'El Teide Volcano, Spain',
          content: 'Photo by Max Rive',
          // You can also provide a URL for the image.
          img: require('@/assets/img/osmo.png')
        }
      ] 
    },
    data() {
      return {
        dialog: false,
        videoId: "-EjDnIXnIGI",
        features: [
          {
            img: require("@/assets/img/osmo.png"),
            title: "Osmosis",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          },
          {
            img: require("@/assets/img/evmos.png"),
            title: "Evmos",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          },
          {
            img: require("@/assets/img/ethereum.png"),
            title: "Ethereum",
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          },
        ],
        products: [
          {
            img: require("@/assets/img/evridge.png"),
            title: "Evridge",
            text: "Explanation about this product"
          },
          {
            img: require("@/assets/img/evridge.png"),
            title: "Mepe",
            text: "Explanation about this product"
          },
          {
            img: require("@/assets/img/evridge.png"),
            title: "Sail",
            text: "Explanation about this product"
          },
          {
            img: require("@/assets/img/evridge.png"),
            title: "QVE",
            text: "Explanation about this product"
          },
          {
            img: require("@/assets/img/evridge.png"),
            title: "SSOYO",
            text: "Explanation about this product"
          }
        ]
      };
    },
    watch: {
      dialog(value) {
        if (!value) {
          this.pause();
        }
      },
    },
    methods: {
      ready(event) {
        this.player = event.target;
      },
      playing(event) {
        // The player is playing a video.
      },
      change() {
        // when you change the value, the player will also change.
        // If you would like to change `playerVars`, please change it before you change `videoId`.
        // If `playerVars.autoplay` is 1, `loadVideoById` will be called.
        // If `playerVars.autoplay` is 0, `cueVideoById` will be called.
        this.videoId = "another video id";
      },
      stop() {
        this.player.stopVideo();
      },
      pause() {
        this.player.pauseVideo();
      },
    },
  };
  </script>

<style scoped>
.product {
}
.section {
  color: white;
}
.products {
  color: white;
  font-size: 50px;
}
#download {
  background-image: url("~@/assets/img/bgDownload.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 700px;
}

#download .container,
#download .row {
  height: 100%;
}


</style>

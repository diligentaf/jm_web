<template>
  <section id="download">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img src="@/assets/img/ill2.svg" class="d-block ml-auto mr-auto" max-width="350px" />
            </v-col>
            <v-col cols="12" sm="8" class="white--text text-left">
              <h1 class="font-weight-light display-2 mb-2">Baixar Demonstração</h1>
              <h1 class="font-weight-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste ex
                animi quod laboriosam vel blanditiis labore alias, aliquid,
                tempora repellendus non.
              </h1>
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
                <p class="subheading ml-2 mb-0">Assista o vídeo</p>
              </div>
              <v-dialog v-model="dialog" max-width="640px">
                <v-card>
                  <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
                </v-card>
              </v-dialog>
              <!-- <v-btn rounded outlined href="https://github.com/Joabsonlg/Landing-Page" target="_blank" large
                color="white" class="mt-4">
                <v-icon class="mr-2">
                  mdi-github
                </v-icon>
                Git Hub
              </v-btn> -->
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>

  export default {
    components: {
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
#download {
  background-image: url("~@/assets/img/bgDownload.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
}

#download .container,
#download .row {
  height: 100%;
}
</style>
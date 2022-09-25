<template>
  <div id="download" class="section">
    <br /> <br />
    <div class="partners">
      <h1 class="text-center pt-6 font-weight-light display-3 white--text cardColor">💻 products 💻</h1>
      <br /> <br />
      <v-container fluid class="text-center">
        <v-row align="center" justify="center">
          <v-card>
            <v-card class="partners">
              <v-img src="@/assets/img/evridge.png" max-height="125"></v-img>
              <v-card-title class="text-h6">
                <div class="partners video d-flex align-center py-4">
                  <a @click.stop="dialog = true" class="playBut">
                    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                      xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/" x="0px" y="0px" width="60px"
                      height="60px" viewBox="0 0 213.7 213.7" xml:space="preserve">
                      <polygon class="triangle" id="XMLID_18_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" points="73.5,62.5 148.5,105.8 73.5,149.1 " />

                      <circle class="circle" id="XMLID_17_" fill="none" stroke-width="7" stroke-linecap="round"
                        stroke-linejoin="round" stroke-miterlimit="10" cx="106.8" cy="106.8" r="103.3" />
                    </svg>
                  </a>
                  <v-btn @click.stop="dialog = true" class="playBut">watch video</v-btn>
                  <v-btn @click="openWeb" class="subheading ml-2 mb-0">open Evridge</v-btn>
                </div>
              </v-card-title>
            </v-card>
          </v-card>
        </v-row>
      </v-container>
    </div>

    <v-container fluid id="features" class="mt-2">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around">
            <!-- <v-col cols="12" class="text-center">
              <h1 class="font-weight-light display-2">Title</h1>
              <h1 class="font-weight-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </h1>
            </v-col> -->
            <v-col cols="12" sm="4" class="text-center" v-for="(feature, i) in features" :key="i">
              <v-hover v-slot:default="{ hover }">
                <v-card class="card" shaped :elevation="hover ? 10 : 4" :class="{ up: hover }">
                  <v-img :src="feature.img" max-width="100px" class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"></v-img>
                  <h1 class="font-weight-regular">{{ feature.title }}</h1>
                  <h4 class="font-weight-regular subtitle-1">
                    {{ feature.text }}
                  </h4>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-dialog v-model="dialog" max-width="640px">
      <v-card>
        <youtube :video-id="videoId" @ready="ready" @playing="playing"></youtube>
      </v-card>
    </v-dialog>
    <div class="svg-border-waves">
      <img src="~@/assets/img/wave2.svg" />
    </div>
  </div>
</template>

<script>

export default {
  components: {
  },
  data() {
    return {
      dialog: false,
      videoId: "-EjDnIXnIGI",
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
    openWeb() {
      window.open('https://evridge.app/#/', '_blank');
    },
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

<style scoped lang="scss">
$main_color: #283e79;

ul {
  font-size: 13px;
  line-height: 1.5em;
  margin: 5px 0 15px;
  padding: 0;

  li {
    list-style: none;
    position: relative;
    padding: 0 0 0 20px;
  }

  li {
    &::before {
      content: "";
      position: absolute;
      left: 0;
      top: 5px;
      width: 10px;
      height: 10px;
      background-color: $main_color;
      border-radius: 50%;
      -moz-border-radius: 50%;
      -webkit-eeborder-radius: 50%;
    }
  }
}

.partnerlist {
  font-size: 30px;
  margin-top: 15px;
}

.partnerimg {
  border: 2px outset;
}

.header {
  background-color: #283e79;
}

.circle1 {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  background-color: #f0f8ff;
  display: flex;
  align-items: center;
  justify-content: center;
}

.circle2 {
  border-radius: 50%;
  width: 100px;
  height: 100px;
  background-color: #e0effc;
  display: flex;
  align-items: center;
  justify-content: center;
}

.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.svg-border-rounded svg {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  color: #f4f7f5;
  z-index: -1;
}

#pricing {
  z-index: 0;
}

.content {
  z-index: 1;
}

svg {
  overflow: hidden;
}

section {
  position: relative;
}

.partners {
  background-color: black;
  color: white;
}
</style>


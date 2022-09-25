<template>
  <section id="hero">
    <!-- <v-parallax dark src="@/assets/img/triangle.gif" height="1400"> -->
    <v-parallax dark src="@/assets/img/black.gif">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6" xl="8">
              <h1 class="display-2 font-weight-bold mb-4">Stake and Earn</h1>
              <h1 class="font-weight-light">
                JM helps investors compound their cryptocurrency investments <br />
                Grow your Crypto with Secure Staking<br />
              </h1>
              <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#features')"
                class="mt-5"
              >
                Networks We Run
                <v-icon class="ml-2">mdi-arrow-down</v-icon>
              </v-btn>
            </v-col>
            <v-col cols="12" md="6" xl="4" class="hidden-sm-and-down"> </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-parallax>
  </section>
</template>

<script>

export default {
  components: {
  },
  data() {
    return {
      dialog: false,
      videoId: "i8IvvHJssWE",
      features: [
        {
          img: require("@/assets/img/osmo.png"),
          title: "Osmosis",
          // text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          link: "https://osmosis.zone/"
        },
        {
          img: require("@/assets/img/evmos.png"),
          title: "Evmos",
          // text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          link: "https://evmos.org/"
        },
        {
          img: require("@/assets/img/ethereum.png"),
          title: "Ethereum",
          // text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          link: "https://ethereum.org/en/"
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
    openWebsite(content) {
      window.open(content, '_blank');
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

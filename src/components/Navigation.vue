<template>
  <div>
    <v-navigation-drawer v-model="drawer" app temporary dark src="@/assets/img/triangle.gif">
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="@/assets/img/SigmaCircle.png" max-width="50px" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Sigma</v-list-item-title>
            <v-list-item-subtitle>🟡Σ🟡</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item v-for="([icon, text, link], i) in items" :key="i" link @click="$vuetify.goTo(link)">
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
            text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app :color="color" :flat="flat" dark class="px-15" :class="{ expand: flat }">
      <v-toolbar-title>
        <v-img src="@/assets/img/SigmaCircle.png" max-width="50px" />
      </v-toolbar-title>
      <v-spacer />
      <!-- moog: logo -->
      <v-card flat class="cardColor d-flex align-center">
        <v-card-text>
          <v-btn color="" icon target="_blank" href="https://twitter.com/sigma_town">
            <v-img src="@/assets/img/icons8-twitter-48.png" max-width="24px" color="" class=""></v-img>
          </v-btn>
          <v-btn color="" icon target="_blank" href="https://discord.gg/DpNzbNn4">
            <v-img src="@/assets/img/icons8-discord-48.png" max-width="24px" color="" class=""></v-img>
          </v-btn>
          <v-btn color="" icon target="_blank" href="https://t.me/sigma_town">
            <v-img src="@/assets/img/icons8-telegram-app-48.png" max-width="24px" color="" class=""></v-img>
          </v-btn>
        </v-card-text>
      </v-card>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="mr-4" v-if="isXs" />
      <div v-else>
        <v-btn text @click="$vuetify.goTo('#hero')">
          <span class="mr-2">Home</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#features')">
          <span class="mr-2">Networks</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#download')">
          <span class="mr-2">Products</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2">Achievements</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">We're Hiring!</span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>


<script>
export default {
  data: () => ({
    feature: [
      {
        img: require("@/assets/img/icons8-discord-48.png"),
      },
      {
        img: require("@/assets/img/icons8-telegram-app-48.png"),
      },
      {
        img: require("@/assets/img/icons8-twitter-48.png"),
      },
    ],
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Home", "#hero"],
      ["mdi-access-point-network", "Network", "#features"],
      ["mdi-code-not-equal-variant", "Products", "#download"],
      ["mdi-code-braces-box", "Achievements", "#pricing"],
      ["mdi-email-outline", "We're Hiring!", "#contact"],
    ],
  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
  },

  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
};
</script>

<style scoped>
.cardColor {
  background-color: rgba(0, 0, 0, 0.0) !important;
  height: 2px !important;
  white-space: nowrap;
  word-break: normal;
  /* overflow: hidden ; */
  text-overflow: ellipsis;
}

.v-toolbar {
  transition: 0.6s;
}

.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>

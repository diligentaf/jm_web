<template>
  <section class="pb-8 partners">
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center partners">
      <v-card-text>
        <v-btn color="black" icon target="_blank" href="https://twitter.com/sigma_town">
          <v-img
            :src="feature[2].img"
            max-width="24px"
            color="white"
            class="d-block ml-auto mr-auto"
            :class="{ 'zoom-efect': hover }"
          ></v-img>
        </v-btn>
        <v-btn color="black" icon target="_blank" href="https://discord.gg/DpNzbNn4">
          <v-img
          :src="feature[0].img"
          max-width="24px"
          color="white"
          class="d-block ml-auto mr-auto"
          :class="{ 'zoom-efect': hover }"
          ></v-img>
        </v-btn> 
        <v-btn color="black" icon target="_blank" href="https://t.me/sigma_town">
          <v-img
          :src="feature[1].img"
            max-width="24px"
            color="white"
            class="d-block ml-auto mr-auto"
            :class="{ 'zoom-efect': hover }"
          ></v-img>
        </v-btn>
      </v-card-text>
 
      <v-divider></v-divider>
 
      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Sigma</strong>
      </v-card-text>
    </v-card>
  </v-footer>
  </section>
</template>
 
<style scoped>
.v-card {
  width: 100%;
}
</style>
 
<script>
export default {
  data: () => ({
    feature: [
        {
          img: require("@/assets/img/icons8-discord-48.png"),
          link: "https://t.me/jmvalidator"
        },
        {
          img: require("@/assets/img/icons8-telegram-app-48.png"),
          link: "https://discord.gg/DpNzbNn4"
        },
        {
          img: require("@/assets/img/icons8-twitter-48.png"),
          link: "https://twitter.com/sigma_town"
        },
      ],
  }),
};
</script>

 <style scoped lang="scss">
.partners {
  background-color: black;
}
</style>
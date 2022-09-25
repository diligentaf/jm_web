<template>
  <section class="pb-8 partners">
  <br/> <br/>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <v-card-text>
        <v-btn color="black" icon target="_blank" href="https://twitter.com/JM_NODE">
          <v-img
            :src="feature[2].img"
            max-width="24px"
            color="white"
            class="d-block ml-auto mr-auto"
          ></v-img>
        </v-btn>
        <v-btn color="black" icon target="_blank" href="https://discord.gg/sWUjDnbu">
          <v-img
          :src="feature[0].img"
          max-width="24px"
          color="white"
          class="d-block ml-auto mr-auto"
          ></v-img>
        </v-btn> 
        <v-btn color="black" icon target="_blank" href="https://t.me/jmnode">
          <v-img
          :src="feature[1].img"
            max-width="24px"
            color="white"
            class="d-block ml-auto mr-auto"
          ></v-img>
        </v-btn>
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
        },
        {
          img: require("@/assets/img/icons8-telegram-app-48.png"),
        },
        {
          img: require("@/assets/img/icons8-twitter-48.png"),
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
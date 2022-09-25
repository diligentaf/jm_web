<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" class="cardColor" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2 white--text">What we stand for</h1>
              <h1 class="font-weight-light display-1 mb-3 white--text">
                <!-- JM Node promises you these 3 things 👇 -->
              </h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center white--text">
                  <v-icon
                    max-width="60px"
                    class="mr-4 white--text"
                  >mdi-check-decagram
                  </v-icon>
                  <p class="text-justify">
                    Secure the Internet of Blockchains
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center white--text">
                  <v-icon
                    max-width="60px"
                    class="mr-4 white--text"
                  >mdi-check-decagram
                  </v-icon>
                  <p class="text-justify">
                    Real-time community engagement
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center white--text">
                  <v-icon
                    max-width="60px"
                    class="mr-4 white--text"
                  >mdi-check-decagram
                  </v-icon>
                  <p class="text-justify">
                    Transparent reward distribution
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/a.gif"
                class="d-block ml-auto mr-auto"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.cardColor {
  background-color: rgba(0, 0, 0, 1.0) !important;
  border-color: white !important;
}
#about {
   background-color: rgba(0, 0, 0, 0.8) !important;
}
</style>

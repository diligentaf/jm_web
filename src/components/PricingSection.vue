
<template>
  <section id="pricing" class="pb-8" >
    <h1 class="text-center pt-6 font-weight-light display-2">Hackathon</h1>
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-card style="width: 100%"  :elevation="hover ? 24 : 20"
          class="mx-auto pa-6">
      
            <!-- <v-divider class="my-6"></v-divider> -->
            <v-row class="text-center">
              <v-col class="col-12 col-sm-6 col-md-4">
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2"  @mouseenter="hover = true"
                        @mouseleave="hover = false">
                          <v-img src="~@/assets/img/polygon.png" ></v-img>           
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h3 my-2" style="color: black">Polygon</div>
                 
                
                    <div class="text-uppercase text-h5 mt-6 blue--text">Prize$ 20,00</div>
                    <v-btn
                        v-bind="size"
                        rounded
                        outlined
                        color="blue"
                        class="mt-6"
                    >
                      Visit Website
                    </v-btn>
                  </v-card-text>
                  <v-divider style="margin-right: -23px" vertical v-if="this.$vuetify.breakpoint.smAndUp"></v-divider>
                </div>
                <v-divider class="mx-4" v-if="!this.$vuetify.breakpoint.smAndUp"></v-divider>
              </v-col>


              <v-col class="col-12 col-sm-6 col-md-4">
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img src="~@/assets/img/evmos.png"/>
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h3 my-2">Evmos</div>
                    
                  
                    <div class="text-uppercase text-h5 mt-6 blue--text">Prize$ 100,00</div>
                    <v-btn
                        v-bind="size"
                        rounded
                        outlined
                        color="blue"
                        class="mt-6"
                    >
                      Visit website
                    </v-btn>
                  </v-card-text>
                  <v-divider style="margin-right: -23px" vertical v-if="this.$vuetify.breakpoint.mdAndUp"></v-divider>
                </div>
                <v-divider class="mx-4" v-if="!this.$vuetify.breakpoint.smAndUp"></v-divider>
              </v-col>


              <v-col class="col-12 col-md-4">
                <v-divider v-if="this.$vuetify.breakpoint.smOnly" class="mx-4"></v-divider>
                <div class="flex-center">
                  <v-card-text>
                    <div class="flex-center">
                      <div class="circle1">
                        <div class="circle2">
                          <v-img src="~@/assets/img/atom.png"/>
                        </div>
                      </div>
                    </div>
                    <div class="text--disabled text-uppercase text-h3 my-2">Atom</div>
                 
                    
                    <div class="text-uppercase text-h5 mt-6 blue--text">Prize$ 500,00</div>
                    <v-btn
                        v-bind="size"
                        rounded
                        outlined
                        color="blue"
                        class="mt-6"
                    >
                      Visit website
                    </v-btn>
                  </v-card-text>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-container><br /><br />


    

    <div class="partners">
      <h1 class="text-center pt-6 font-weight-light display-2">Partners</h1>
      <v-container fluid>
        <v-row align="center" justify="center">
          <v-col cols="8">
            <v-card style="width: 100%; background-color: black;"   :elevation="hover ? 24 : 6"
            class="mx-auto pa-10">

              <v-row class="text-center">

                <v-col>
                  <div class="flex-center">
                    <v-card-text>
                      <div class="flex-center">
                        <div >
                          <div class="partnerimg">
                            <v-img src="~@/assets/img/bwl_logo.png" light max-width="200"></v-img>           
                          </div>
                        </div>
                      </div>
                      <div class="partnerlist">Blockwave Labs</div>
                      <v-hover v-slot="{ hover }">
                        <v-btn
                            v-bind="size"
                            rounded
                            outlined
                            tile
                            color="blue"
                            class="mt-6"
                            :style="{ 'background-color': hover ? 'white' : 'black' }"
                        >
                          Visit Website
                        </v-btn>
                      </v-hover>
                      
                    </v-card-text>
                    <!-- <v-divider style="margin-right: -23px" vertical v-if="this.$vuetify.breakpoint.smAndUp"></v-divider> -->
                  </div>
                  <v-divider class="mx-4" v-if="!this.$vuetify.breakpoint.smAndUp"></v-divider>
                </v-col>
  
  
                <v-col>
                  <div class="flex-center">
                    <v-card-text>
                      <div class="flex-center">
                        <div>
                          <div  class="partnerimg">
                            <v-img src="~@/assets/img/nonce_logo.png" max-width="200" />
                          </div>
                        </div>
                      </div>
                      <div class="partnerlist">Nonce</div>
              
                      <v-hover v-slot="{ hover }">
                        <v-btn
                            v-bind="size"
                            rounded
                            outlined
                            tile
                            elevation="100"
                            color="primary"
                            class="mt-6"
                            :style="{ 'background-color': hover ? 'white' : 'black' }"
                        >
                          Visit Website
                        </v-btn>
                      </v-hover>
                    </v-card-text>
                    <!-- <v-divider style="margin-right: -23px" vertical v-if="this.$vuetify.breakpoint.mdAndUp"></v-divider> -->
                  </div>
                  <v-divider class="mx-4" v-if="!this.$vuetify.breakpoint.smAndUp"></v-divider>
                </v-col>
              </v-row>
            </v-card>
          </v-col>


        </v-row>
      </v-container>
    </div>
  
  </section>
</template>

<style lang="scss">
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
</style>

<style scoped>
.partnerlist {
  color: white;
  font-size: 30px;
  margin-top: 15px;
}
.partnerimg {
  border: 2px outset white;
}
.header {
  background-color: #283e79;
  color: white;
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

<script>
export default {
  data: () => ({
    planos: [
      {
        title: "Básico",
        price: "R$100,00",
        img: "f1.png",
        features: [
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 1",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 2",
          },
          {
            icon: {
              text: "mdi-cancel",
              color: "red",
            },
            text: "Feature 3",
          },
          {
            icon: {
              text: "mdi-cancel",
              color: "red",
            },
            text: "Feature 4",
          },
        ],
      },
      {
        title: "Padrão",
        price: "R$150,00",
        img: "f2.png",
        features: [
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 1",
            color: "success",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 2",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 3",
            color: "success",
          },
          {
            icon: {
              text: "mdi-cancel",
              color: "red",
            },
            text: "Feature 4",
          },
        ],
      },
      {
        title: "Premium",
        price: "R$250,00",
        img: "f3.png",
        features: [
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 1",
            color: "success",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 2",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 3",
            color: "success",
          },
          {
            icon: {
              text: "mdi-check",
              color: "success",
            },
            text: "Feature 4",
            color: "success",
          },
        ],
      },
    ],
  }),
  computed: {
    size() {
      const size = {md: "large", xl: "x-large"}[
          this.$vuetify.breakpoint.name
          ];
      return size ? {[size]: true} : {};
    }
  },
};
</script>
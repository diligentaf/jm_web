<template>
  <section class="pb-8" id="contact">
    <div class="partners">
      <h1 class="text-center pt-6 font-weight-light display-2">JMNODE is Hiring</h1><br></br>
      <v-container fluid class="text-center">
        <v-row align="center" justify="center">
          <v-card-text class="white--text pt-0 subtitle-1">
            Our goal is to serve the world with sustainable blockchain ecosystem.
          </v-card-text>
          <v-card-text class="white--text pt-0 subtitle-1">
            We believe working at JMNODE will push your limits and enable you to work with amazing people.
          </v-card-text>
          <v-card-text class="white--text pt-0 subtitle-1">
            We believe learning and communication are equally as valuable as engineering and design talent.
            currently distributed across the United States and Asia.
          </v-card-text>
          <v-card-text class="white--text pt-0 subtitle-1">
            Our team is currently distributed across the United States and Asia.
          </v-card-text>
          <v-card-text class="white--text pt-0 subtitle-1">
            Contact us on Twitter and Discord and please consider checking for job openings
          </v-card-text>
          <v-card-text class="white--text pt-0 subtitle-1">
            ⬇️
          </v-card-text>
        </v-row>
      </v-container>
    </div>

  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}
</style>

<script>
// import {db} from '@/main'

export default {
  data: () => ({
    icons: ["fa-facebook", "fa-twitter", "fa-linkedin", "fa-instagram"],
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "Name is an essential field",
      (v) => (v && v.length >= 1) || "Name should be longer than 1 letter",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "Email is an essential field",
      (v) => /.+@.+\..+/.test(v) || "Email should be valid",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "Message is an essential field",
      (v) => (v && v.length >= 10) || "Message should be longer than 10 letters",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  methods: {
    submit() {
      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensagem enviada com sucesso"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Erro ao enviar mensagem"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    }
  }
};
</script>

<style scoped lang="scss">
.cardColor {
  background-color: rgba(0, 0, 0, 0.5) !important;
  border-color: white !important;
}

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
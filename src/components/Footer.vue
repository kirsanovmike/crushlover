<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <!-- <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text> -->

      <v-card-text class="white--text pt-0">
        Thank you for being with us. We try to make the best services for you.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>CRUSH LOVER WEB</strong>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        <v-btn class="ma-2" outlined color="white" @click="openPrivacyPolicy">
          Privacy Policy
        </v-btn>
        <!-- <v-btn class="ma-2" outlined color="white" @click="openPrivacyPolicy">
          Privacy Policy
        </v-btn>
        <v-btn class="ma-2" outlined color="white" @click="openTermsAndConditions">
          Terms & Conditions
        </v-btn> -->
        <v-btn
          class="ma-2"
          outlined
          color="white"
          @click="openTermsAndConditions"
        >
          Terms & Conditions
        </v-btn>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>
.v-card {
  width: 100%;
}
</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "",
      },
      {
        text: "mdi-twitter",
        link: "",
      },
      {
        text: "mdi-linkedin",
        link: "",
      },
      {
        text: "mdi-instagram",
        link: "https://instagram.com/joabson_arley/",
      },
    ],
  }),
  methods: {
    openPrivacyPolicy() {
      window
        .open(
          `${
            process.env.NODE_ENV === "production" ? "/crushlover/" : "/"
          }?document=privacy-policy`,
          "_blank"
        )
        .focus();
    },
    openTermsAndConditions() {
      window
        .open(
          `${
            process.env.NODE_ENV === "production" ? "/crushlover/" : "/"
          }?document=terms-of-use`,
          "_blank"
        )
        .focus();
    },
  },
};
</script>

<template>
    <v-card>
    <v-bottom-navigation>
      <v-btn
        color="yellow"
        text
      >

        <v-icon>mdi-home-variant</v-icon>
      </v-btn>

      <v-btn
        color="yellow"
        text
      >

        <v-icon>mdi-gift</v-icon>
      </v-btn>

      <v-btn
        color="yellow"
        text
      >

        <v-icon>mdi-currency-cny</v-icon>
      </v-btn>

      <v-btn
        color="yellow"
        text
      >

        <v-icon>mdi-message-processing-outline</v-icon>
      </v-btn>

      <v-btn
        color="yellow"
        text
      >

        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-card>
</template>

<style>
  @media only screen and (min-width: 800px) {
        .v-bottom-navigation .v-bottom-navigation--active .v-theme--dark .v-bottom-navigation--density-default {
            height: 100px;
        }
        .v-bottom-navigation .v-bottom-navigation__content > .v-btn {
          min-width: 180px
        }
    }
</style>
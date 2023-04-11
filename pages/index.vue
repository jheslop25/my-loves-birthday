<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="logo py-4 d-flex justify-center">
        <VuetifyLogo />
      </v-card>
      <v-card>
        <v-row class="my-2 mx-2" justify="center">
          <h1>Happy Birthday Mayra Paola My Love<v-icon>mdi-heart</v-icon></h1>
        </v-row>

        <v-row class="my-2 mx-2" justify="center">
          <p>{{ remainingTime.text }}</p>
        </v-row>
        <v-card-actions v-if="showButton">
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire"> Continue </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  computed: {
    // a function that calculates the remaining time until April 11th 2023 at 8:00 pm (GMT-5) and display the date in a human readable format
    remainingTime() {
      const now = new Date()
      const birthday = new Date(2023, 4, 11, 20, 0, 0, 0)
      const difference = birthday.getTime() - now.getTime()
      const remainingTime = {
        days: Math.floor(difference / (1000 * 60 * 60 * 24)),
        hours: Math.floor(
          (difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
        ),
        minutes: Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60)),
        seconds: Math.floor((difference % (1000 * 60)) / 1000),
      }

      return {
        data: remainingTime,
        text: `There are 0 days, ${remainingTime.hours} hours, ${remainingTime.minutes} minutes and ${remainingTime.seconds} seconds until your birthday present reveal! :)`,
      }
    },
    showButton() {
      return this.remainingTime.data.days <= 0
    },
  },
}
</script>

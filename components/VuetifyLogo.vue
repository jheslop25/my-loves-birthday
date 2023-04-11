<template>
  <img class="vuetify-logo" alt="Vuetify Logo" :src="require('~/static/IMG_5750.jpeg')" />
</template>

<style>
.vuetify-logo {
  height: 380px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>

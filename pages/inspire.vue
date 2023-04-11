<template>
  <v-row>
    <v-col class="text-center">
      <p v-if="!show">
        My Dearest, <br />
        <br />
        For your birthday I want to give you the best gift I can give you, which
        is my love. <br />
        <br />
        Unfortunately you can't unwrap love... or can you? ;) <br />

        <br />
        So I decided to give you something that you also can't really unwrap,
        but that you can enjoy for a long time. <br />
        <br />

        It's something I know you have really really been wanting and I hope you
        enjoy it!
        <br />
        This gift is special because it's something that we can enjoy together.
        <br />
        <br />
        I love you very much! <br />
        <v-icon>mdi-heart</v-icon> <v-icon>mdi-heart</v-icon>
      </p>
      <v-row v-if="!show" class="my-4 mx-2" justify="center">
        <v-btn @click="show = !show" color="primary"
          >SHOW ME THE PRESENT!!</v-btn
        >
      </v-row>
      <v-row v-if="show" class="my-3 mx-2" justify="center">
        <v-col>
          <v-row class="my-2 mx-2" justify="center">
            <h1>Happy Birthday Mayra Paola My Love<v-icon>mdi-heart</v-icon></h1>
          </v-row>
          <v-row class="my-3 mx-2">
            <v-img width="200" src="https://static.wixstatic.com/media/nsplsh_6c64345675625758547549~mv2_d_5472_3648_s_4_2.jpg/v1/fill/w_559,h_887,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/nsplsh_6c64345675625758547549~mv2_d_5472_3648_s_4_2.jpg"></v-img>
            <p class="my-3">Click the link below for full details but I think you can guess what this is so far. :)</p>
          </v-row>
          <v-row class="my-2 mx-2" justify="center">
            <v-btn
              color="success"
              href="https://www.cozumeldiveschool.mx/beginners"
              >More Info</v-btn
            >
          </v-row>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'InspirePage',
  data: () => ({
    show: false,
  }),
}
</script>

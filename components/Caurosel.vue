<template>
  <v-carousel cycle height="500" hide-delimiter-background show-arrows-on-hover>
    <template v-slot:prev="{ on, attrs }">
      <v-btn color="success" v-bind="attrs" v-on="on"
        ><v-icon>mdi-arrow-collapse-right</v-icon></v-btn
      >
    </template>
    <template v-slot:next="{ on, attrs }">
      <v-btn color="info" v-bind="attrs" v-on="on"
        ><v-icon>mdi-arrow-collapse-left</v-icon></v-btn
      >
    </template>
    <v-carousel-item v-for="(slide, i) in slides" :key="i">
      <v-sheet :color="colors[i]" height="100%">
        <v-row class="fill-height" align="center" justify="center">
          <v-img
            :src="`${slide}`"
            :lazy-src="`${slide}`"
            aspect-ratio="1"
            max-height="500px"
            max-width="100%"
          ></v-img>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      slides: ["./1.jpg", "./2.jpg", "./3.jpg"],
      colors: ["blue", "red", "pink"],
    };
  },
};
</script>

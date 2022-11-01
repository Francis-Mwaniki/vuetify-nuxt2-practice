<template>
  <v-app>
    <v-container class="pa-1" fluid>
      <v-row no-gutters>
        <v-col class="item" v-for="slide in slides" cols="12" sm="6" md="4">
          <v-card class="mx-auto" max-width="344">
            <v-img :src="slide" height="300px"></v-img>

            <v-card-title> Top western road trips </v-card-title>

            <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle>

            <v-card-actions>
              <v-btn color="orange lighten-2" text> Explore </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  I'm a thing. But, like most politicians, he promised more than he could
                  deliver. You won't have time for sleeping, soldier, not with all the bed
                  making you'll be doing. Then we'll go with that data file! Hey, you add
                  a one and two zeros to that or we walk! You're going to do his laundry?
                  I've got to find a way to escape.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      show: false,
      slides: ["./1.jpg", "./2.jpg", "./3.jpg", "./1.jpg", "./2.jpg", "./3.jpg"],
    };
  },
};
</script>

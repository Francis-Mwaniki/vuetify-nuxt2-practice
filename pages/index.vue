<template>
  <main>
    <NavigationVue />
    <v-spacer></v-spacer>
    <CauroselVue />
    <v-spacer></v-spacer>
    <cardVue />
  </main>
</template>

<script>
import CauroselVue from "../components/Caurosel.vue";
import NavigationVue from "../components/Navigation.vue";
import cardVue from "../components/card.vue";

export default {
  name: "IndexPage",
  components: {
    NavigationVue,
    CauroselVue,
    cardVue,
  },
};
</script>

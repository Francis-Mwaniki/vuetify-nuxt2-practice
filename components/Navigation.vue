<template>
  <v-card class="mx-auto overflow-hidden" width="100%" app>
    <v-app-bar color="indigo" dark>
      <v-btn color="primary" class="ma-2 rounded-lg" dark @click.stop="dialog = true">
        <v-icon>mdi-view-sequential</v-icon>
      </v-btn>

      <v-dialog v-model="dialog" max-width="290">
        <v-card class="pa-16">
          <v-list nav dense>
            <v-list-item-group
              v-model="group"
              active-class="deep-purple--text text--accent-4"
            >
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Home</v-list-item-title>
              </v-list-item>

              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-account</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Account</v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-dialog>

      <v-toolbar-title>
        <v-list-item-icon>
          <v-icon>mdi-lock</v-icon>
        </v-list-item-icon>
        Dashboard</v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-toolbar-title>
        <dialogVue />
      </v-toolbar-title>
    </v-app-bar>
  </v-card>
</template>
<script>
import dialogVue from "./dialog.vue";
export default {
  components: {
    dialogVue,
  },
  data() {
    return {
      drawer: false,
      group: false,
      dialog: false,
    };
  },
};
</script>

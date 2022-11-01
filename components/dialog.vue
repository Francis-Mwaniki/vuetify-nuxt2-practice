<template>
  <v-col cols="auto">
    <v-dialog transition="dialog-top-transition" max-width="600">
      <template v-slot:activator="{ on, attrs }">
        <v-btn color="primary" v-bind="attrs" v-on="on">
          <v-icon>mdi-account</v-icon>
        </v-btn>
      </template>
      <template v-slot:default="dialog">
        <v-card>
          <v-toolbar color="primary" dark>Add account</v-toolbar>
          <v-card-text>
            <div class="pa-12">
              <!-- st -->
              <form>
                <v-text-field
                  v-model="name"
                  :error-messages="nameErrors"
                  :counter="10"
                  label="Name"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="email"
                  :error-messages="emailErrors"
                  label="E-mail"
                  required
                ></v-text-field>
                <v-select
                  v-model="select"
                  :items="items"
                  :error-messages="selectErrors"
                  label="Item"
                  required
                ></v-select>
                <v-checkbox
                  v-model="checkbox"
                  :error-messages="checkboxErrors"
                  label="Do you agree?"
                  required
                ></v-checkbox>

                <v-btn class="mr-4" @click="submit"> submit </v-btn>
                <v-btn @click="clear"> clear </v-btn>
              </form>
              <!-- end -->
            </div>
          </v-card-text>
          <v-card-actions class="justify-end">
            <v-btn text @click="dialog.value = false">Close</v-btn>
          </v-card-actions>
        </v-card>
      </template>
    </v-dialog>
  </v-col>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      select: "",
      name: "",
      email: "",
      phoneNumber: "",
      checkbox: "",
      items: ["hello", "hello 2", "hello 3"],
    };
  },
};
</script>

<style></style>

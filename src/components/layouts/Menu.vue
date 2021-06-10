
<template >
  <v-card dark color="grey lighten-4" flat tile>
    <v-toolbar color="warning">
      <v-app-bar-nav-icon
        @click="$emit('update:show_bar', !show_bar)"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>Web-Home</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color="success">
        Login
        <v-icon>login</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>


<script>
export default {
  name: "Menu",

  data() {
    return {};
  },
  props: {
    show_bar: {
      type: Boolean,
    },
  },
};
</script>

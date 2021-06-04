<template>
  <v-navigation-drawer
    v-model="show_bar"
    absolute
    temporary
    @click="$emit('update:show_bar', false)"
  >
    <v-list-item>
      <v-list-item-avatar>
        <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
      </v-list-item-avatar>

      <v-list-item-content>
        <v-list-item-title>Hector Eduardo</v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideBar",

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

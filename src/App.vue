<template>
  <v-app>
    <!-- barra de menu -->
    <Menu :show_bar.sync="show_bar"> </Menu>
    <!-- End of Barra de menu -->

    <v-main>
      <!-- Side Bar -->
      <SideBar :show_bar="show_bar"></SideBar>
      <!-- End of Side Bar -->
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import Menu from "@/components/Menu";
import SideBar from "@/components/Side-bar";

export default {
  name: "App",

  data() {
    return {
      show_bar: false,
    };
  },
  computed: {},
  components: {
    Menu,
    SideBar,
  },
};
</script>

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
    <Footer></Footer>
  </v-app>
</template>

<script>
import Menu from "@/components/layouts/Menu";
import SideBar from "@/components/layouts/Side-bar";
import Footer from "@/components/layouts/Footer";

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
    Footer,
  },
};
</script>

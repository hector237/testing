<template>
  <v-navigation-drawer v-model="show_menu" absolute temporary>
    <v-list>
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
        </v-list-item-avatar>
      </v-list-item>

      <v-list-item link>
        <v-list-item-content>
          <v-list-item-title class="text-h6"> John Leider </v-list-item-title>
          <v-list-item-subtitle>john@vuetifyjs.com</v-list-item-subtitle>
        </v-list-item-content>

        <v-list-item-action>
          <v-icon>menu-down</v-icon>
        </v-list-item-action>
      </v-list-item>
    </v-list>
    <v-divider></v-divider>
    <v-list nav dense>
      <!-- sub-groups of menu -->
      
          <v-list-item-content>
            <v-list-item

          
          
          to="/"
        >
          <v-list-item-icon>
            <v-icon>dashboard</v-icon>
          </v-list-item-icon>
          <v-list-item-title> Dashboard </v-list-item-title>
        </v-list-item>
      
      <v-list-group no-action sub-group>
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title>Impuestos</v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="(item, i) in payments"
          :key="i"
          link
          :to="item.routes"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-title v-text="item.text"> </v-list-item-title>
        </v-list-item>
      </v-list-group>

      <v-list-group no-action sub-group>
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title>User</v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item v-for="(item, i) in user" :key="i" link class="">
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-title v-text="item.text"></v-list-item-title>
        </v-list-item>
      </v-list-group>
      <!-- end sub-groups of menu -->
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideBar",

  data() {
    return {
      selectedItem: 0,
      payments: [
        {
          text: "Electricidad",
          icon: "electrical_services",
          routes: "/payments/energy",
        },
        { text: "Comida", icon: "restaurant", routes: "/payments/food" },
        { text: "Telefono", icon: "phone", routes: "/payments/phone" },
        { text: "Gastos", icon: "attach_money", routes: "/payments/gastos" },
      ],

      user: [
        { text: "Agenda", icon: "event", routes: "" },
        { text: "Tareas", icon: "task", routes: "" },
        { text: "Contactos", icon: "info", routes: "" },
        { text: "Info", icon: "account_circle", routes: "" },
      ],
      show: false,
    };
  },
  computed: {
    show_menu: {
      get() {
        return this.show_bar;
      },
      set(show_bar) {
        let side_bar = show_bar;
        this.$emit("showMenu", side_bar);
      },
    },
  },
  props: {
    show_bar: {
      type: Boolean,
    },
  },
};
</script>

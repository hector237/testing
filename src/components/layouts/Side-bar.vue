<template>
  <v-navigation-drawer
    v-model="show_bar"
    absolute
    temporary
    @click="$emit('update:show_bar', false)"
  >
    <v-card class="mx-auto" width="256" tile>
      <v-navigation-drawer permanent>
        <v-list>
          <v-list-item>
            <v-list-item-avatar>
              <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
            </v-list-item-avatar>
          </v-list-item>

          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title class="text-h6">
                John Leider
              </v-list-item-title>
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
          <v-list-group no-action sub-group>
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Impuestos</v-list-item-title>
              </v-list-item-content>
            </template>

            <v-list-item v-for="(item, i) in payments" :key="i" link>
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item>
          </v-list-group>

          <v-list-group no-action sub-group>
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Actions</v-list-item-title>
              </v-list-item-content>
            </template>

            <v-list-item v-for="(item, i) in user" :key="i" link>
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item>
          </v-list-group>
          <!-- end sub-groups of menu -->
        </v-list>
      </v-navigation-drawer>
    </v-card>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideBar",

  data() {
    return {
      selectedItem: 0,
      payments: [
        { text: "Electricidad", icon: "electrical_services" },
        { text: "Comida", icon: "restaurant" },
        { text: "Telefono", icon: "phone" },
        { text: "Gastos", icon: "attach_money" },
      ],
      payme: [
        { text: "Dashboard", icon: "dashboard" },
        { text: "Impuestos", icon: "payments" },
        { text: "Usuario", icon: "account_circle" },
      ],
      user: [
        { text: "Agenda", icon: "event" },
        { text: "Tareas", icon: "task" },
        { text: "Contactos", icon: "info" },
        { text: "Info", icon: "account_circle" },
      ],
    };
  },
  props: {
    show_bar: {
      type: Boolean,
    },
  },
};
</script>

<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="6" md="6" lg="3" color="primary">
        <v-card elevation="4" color="">
          <v-card-title> Dinero gastado </v-card-title>
          <v-divider></v-divider>
          <v-card-text headline> 5600 </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6" md="6" lg="3">
        <v-card elevation="4">
          <v-card-title> Impuestos </v-card-title>
          <v-divider></v-divider>
          <v-card-text headline> 1200 </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6" md="6" lg="3">
        <v-card elevation="4" shaped>
          <v-card-title> Ultimo mes </v-card-title>
          <v-divider></v-divider>
          <v-card-text headline> 5600 </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6" md="6" lg="3">
        <v-card elevation="4" shaped>
          <v-card-title> Contactos </v-card-title>
          <v-divider></v-divider>
          <v-card-text headline> 5600 </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <!-- charts -->
    <v-row>
      <v-col cols="12" md="" lg="6">
        <lineChart />
      </v-col>

      <v-col cols="12" md="" lg="6">
        <lineChart />
      </v-col>
    </v-row>
    <!-- end charts -->
    <!-- calendar - task -->
    <v-row>
      <!-- task -->
      <v-col cols="12" md="12" lg="6">
        <v-card height="486">
          <v-toolbar color="warning">
            <v-card-title> Tareas pendientes </v-card-title>
            <v-spacer></v-spacer>
            <v-btn fab color="success" medium icon>
              <v-icon>add</v-icon>
            </v-btn>
            <v-btn fab color="success" medium icon>
              <v-icon>refresh</v-icon>
            </v-btn>
          </v-toolbar>
          <v-card-text>
            <v-list>
              <v-list-item-group>
                <v-list-item>
                  <template v-slot:default="{ active }">
                    <v-list-item-action>
                      <v-checkbox :input-value="active"></v-checkbox>
                    </v-list-item-action>

                    <v-list-item-content>
                      <v-list-item-title>Sound</v-list-item-title>
                      <v-list-item-subtitle
                        >Auto-update apps at any time. Data charges may
                        apply</v-list-item-subtitle
                      >
                    </v-list-item-content>
                  </template>
                </v-list-item>
                <!-- end task -->
                <!-- examples -->
                <v-list-item>
                  <template v-slot:default="{ active }">
                    <v-list-item-action>
                      <v-checkbox :input-value="active"></v-checkbox>
                    </v-list-item-action>

                    <v-list-item-content>
                      <v-list-item-title>tarea </v-list-item-title>
                      <v-list-item-subtitle
                        >esto es un ejemplo de panel de tareas para mostrar
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </template>
                </v-list-item>
                <v-list-item>
                  <template v-slot:default="{ active }">
                    <v-list-item-action>
                      <v-checkbox :input-value="active"></v-checkbox>
                    </v-list-item-action>

                    <v-list-item-content>
                      <v-list-item-title>Tarea </v-list-item-title>
                      <v-list-item-subtitle
                        >Auto-update apps at any time. Data charges may
                        apply</v-list-item-subtitle
                      >
                    </v-list-item-content>
                  </template>
                </v-list-item>
                <!-- end example  -->
              </v-list-item-group>
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
      <!-- end task -->
      <!-- calendar -->
      <v-col cols="12" md="" lg="6">
        <calendar />
      </v-col>

      <!-- end calendar -->
    </v-row>
    <!-- end calendar - task -->
  </v-container>
</template>

<script>
import lineChart from "@/components/tools/charts/line_chart";
import calendar from "@/components/tools/calendar/calendar";

export default {
  name: "Home",

  components: {
    lineChart,
    calendar,
  },
};
</script>

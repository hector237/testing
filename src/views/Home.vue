<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="6" lg="3">
        <v-card elevation="2" shaped>
          <v-card-title>
            <p>Lorem ipsum dolor sit.</p>
          </v-card-title>
          <v-card-text headline>
            <p>5600</p>
            <p>/</p>
            <p>1000</p>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" md="6" lg="3">
        <v-card elevation="2" shaped>
          <v-card-title>
            <p>Lorem ipsum dolor sit.</p>
          </v-card-title>
          <v-card-text headline>
            <p>5600</p>
            <p>/</p>
            <p>1000</p>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" md="6" lg="3">
        <v-card elevation="2" shaped>
          <v-card-title>
            <p>Lorem ipsum dolor sit.</p>
          </v-card-title>
          <v-card-text headline>
            <p>5600</p>
            <p>/</p>
            <p>1000</p>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" md="6" lg="3">
        <v-card elevation="2" shaped>
          <v-card-title>
            <p>Lorem ipsum dolor sit.</p>
          </v-card-title>
          <v-card-text headline>
            <p>5600</p>
            <p>/</p>
            <p>1000</p>
          </v-card-text>
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
      <v-col cols="12" md="4" lg="6">
        <lineChart />
      </v-col>
      <!-- end task -->
      <!-- calendar -->
      <v-col class="d-none d-lg-block" cols="12" md="8" lg="6">
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

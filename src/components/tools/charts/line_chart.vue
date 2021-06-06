<template>
  <v-row>
    <v-col cols="12">
      <v-card elevation="4" shaped>
        <v-card-title>Consumo de energia</v-card-title>
        <v-divider></v-divider>
        <v-card-text>
          <v-sparkline
            color="error"
            height="100"
            padding="12"
            stroke-linecap="round"
            smooth="0"
            auto-draw
            auto-draw-easing="ease"
            line-width="0.9"
            :labels="values"
            :value="values"
          >
          </v-sparkline>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-card-text
            ><p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aliquam
              iste est natus accusamus!
            </p></v-card-text
          >
          <v-btn depressed color="primary" fab>
            <v-icon>arrow_right_alt</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "lineChart",

  data() {
    return {
      values: [1, 2, 66, 1, 55, 88, 44, 99, 33, 55, 99, 11, 2],
    };
  },

  components: {},
};
</script>
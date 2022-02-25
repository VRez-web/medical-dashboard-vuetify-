<template>
  <v-card flat color="transparent" class="mt-n5">
    <v-toolbar color="rgba(0,0,0,0)" flat class="py-4">
      <v-toolbar-title>History Survey</v-toolbar-title>
    </v-toolbar>
    <line-chart
        :chart-id="chartId"
        :width="width"
        heigth="200"
        :css-classes="cssClasses"
        :styles="styles"
        :plygins="plugins"
    />
  </v-card>
</template>

<script>
import LineChart from "@/chart/LineChart";

export default {
  name:"HistoryChart",
  components: {
    LineChart
  },
  props: {
    chartId: {
      type: String,
      default: "line-chart",
    },
    width: {
      type: Number,
      default: 400,
    },
    height: {
      type: Number,
      default: 100,
    },
    cssClasses: {
      default: "",
      type: String,
    },
    styles: {
      type: Object,
      default: () => {
      },
    },
    plugins: {
      type: Array,
      default: () => {
      },
    },
  },
}
</script>

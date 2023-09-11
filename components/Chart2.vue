<template>
  <div class="chart" :id="id"></div>
</template>

<script setup>
import { init } from "echarts";
let chart;

const props = defineProps({
  id: String,
});

let option = {
  xAxis: {
    type: "category",
    data: ["06/09", "07/09", "08/09", "09/09", "10/09", "11/09", "12/09"],
    axisLabel: {
      rotate: 90,
    },
    name: "Date",
    nameLocation: "center",
    nameTextStyle: {
      fontSize: 14,
      fontWeight: 500,
      padding: [40, 0],
    },
  },
  yAxis: {
    type: "value",
    name: "Price",
    nameLocation: "center",
    nameTextStyle: {
      fontSize: 14,
      fontWeight: 500,
      padding: [20, 0],
    },
  },
  series: [
    {
      data: [150, 230, 224, 218, 135, 147, 260],
      type: "line",
      name: "USDT",
      color: "#0088ff",
    },
    {
      data: [146, 290, 168, 200, 100, 135, 315],
      type: "line",
      name: "LME",
      color: "#4c4c4c",
    },
  ],

  legend: {
    type: "plain",
  },

  tooltip: {
    trigger: "axis",
  },
};

onMounted(() => {
  chart = init(document.getElementById(props.id));
  chart.setOption(option);
});
</script>

<style lang="scss" scoped>
.chart {
  width: 100vw;
  height: 500px;
  padding: 20px;
}
</style>

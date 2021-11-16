<template>
  <div class="container flex flex-col mx-auto items-center">
      <h2 class="text-gray-500 m-3 mt-10">Hanns Care Analyze</h2>
      <p class="text-gray-500 text-xs mb-5" >User using HannsCare APP function click times record</p>
        <div style="max-width: 400px">
        <vue3-chart-js v-bind="{ ...pieChart }" />
    </div>
  </div>
</template>

<script>
import Vue3ChartJs from "@j-t-mcc/vue3-chartjs";

export default {
  name: "App",
  components: {
    Vue3ChartJs,
  },
  setup() {
    const pieChart = {
      type: "pie",
      data: {
        labels: ["Step", "Distance", "Sleep"],
        datasets: [
          {
            backgroundColor: [
              'rgb(75, 192, 192)',
              'rgb(255, 205, 86)',
              'rgb(54, 162, 235)',
              'rgb(255, 99, 132)',
            ],
            data: [80, 20, 40],
          },
        ],
      },
    };

    return {
      pieChart,
    };
  },
};
</script>

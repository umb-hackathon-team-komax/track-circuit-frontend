<template>
  <div class="rounded border md:shadow">
    <div class="px-4 py-4">
      <vue3-chart-js v-bind="{ ...getChartOptions }" />
    </div>
  </div>
</template>

<script>
import Vue3ChartJs from "@j-t-mcc/vue3-chartjs";

export default {
  components: {
    Vue3ChartJs,
  },
  data() {
    return {
      output: [
        {
          time: new Date(),
          drilled: 12,
          notdrilled: 29,
        },
        {
          time: new Date().setHours(-24),
          drilled: 6,
          notdrilled: 13,
        },
        {
          time: new Date().setHours(-48),
          drilled: 35,
          notdrilled: 21,
        },
        {
          time: new Date().setHours(-72),
          drilled: 23,
          notdrilled: 83,
        },
        {
          time: new Date().setHours(-96),
          drilled: 26,
          notdrilled: 34,
        },
      ],
    };
  },
  beforeMount() {
      
    const barChart = {
      type: "bar",
      options: {
        min: 0,
        max: 100,
        responsive: true,
        plugins: {
          legend: {
            position: "bottom",
          },
        },
        scales: {
          x: {
            stacked: true,
          },
          y: {
            stacked: true,
            min: 0,
            ticks: {
              callback: function (value) {
                return `${value}`;
              },
            },
          },
        },
      },
      data: {
        labels: this.output.map((d) => d.toString()),
        datasets: [
          {
            label: "drilled",
            backgroundColor: ["#396999"],
            data: this.output.map((d) => d.drilled),
          },
          {
            label: "not drilled",
            backgroundColor: ["#F04D55"],
            data: this.output.map((d) => d.notdrilled),
          },
        ],
      },
    };
    return {
      barChart,
    };
  },
  computed: {
    getChartOptions() {
      return {
        type: "bar",
      options: {
        min: 0,
        max: 100,
        responsive: true,
        plugins: {
          legend: {
            position: "bottom",
          },
        },
        scales: {
          x: {
            stacked: true,
          },
          y: {
            stacked: true,
            min: 0,
            ticks: {
              callback: function (value) {
                return `${value}`;
              },
            },
          },
        },
      },
      data: {
        labels: this.output.map((d) => d.toString()),
        datasets: [
          {
            label: "drilled",
            backgroundColor: ["#396999"],
            data: this.output.map((d) => d.drilled),
          },
          {
            label: "not drilled",
            backgroundColor: ["#F04D55"],
            data: this.output.map((d) => d.notdrilled),
          },
        ],
      },
    }
  },
  }
};
</script>

<style>
</style>
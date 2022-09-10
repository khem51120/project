<template>
  <div class="wrapper_page">
    <h1 class="mb-10">บันทึกหน่วยไฟฟ้า</h1>
    <highcharts v-if="showing" :options="chartOptions"></highcharts>
  </div>
</template>

<script>
import { Chart } from "highcharts-vue";

export default {
  components: {
    highcharts: Chart,
  },

  data() {
    return {
      showing: true,
      chartOptions: {
        // title: {
        //   text: "ช่วงเวลารถเข้า/ออก",
        // },
        // yAxis: {
        //   title: {
        //     text: "จำนวนรถ",
        //   },
        // },
        chart: {
          height: this.height - 30,
        },
        xAxis: {
          categories: [
            "Jan",
            "Feb",
            "Mar",
            "Apr",
            "May",
            "Jun",
            "Jul",
            "Aug",
            "Sep",
            "Oct",
            "Nov",
            "Dec",
          ],
        },
        legend: {
          layout: "vertical",
          align: "right",
          verticalAlign: "middle",
        },

        series: [
          {
            name: "A",
            data: [1, 2, 3, 1, 5, 4, 3, 2],
          },
          {
            name: "B",
            data: [3, 4, 5, 6, 1, 4, 6, 3, 4, 5],
          },
        ],

        responsive: {
          rules: [
            {
              condition: {
                maxWidth: 500,
              },
              chartOptions: {
                legend: {
                  layout: "horizontal",
                  align: "center",
                  verticalAlign: "bottom",
                },
              },
            },
          ],
        },
        colors: ["#3336FF", "#41EDE8"],
      },
    };
  },
};
</script>

<style></style>

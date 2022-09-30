<template>
  <div class="wrapper_page">
    <h1 class="mb-10">บันทึกหน่วยไฟฟ้า</h1>
    <div class="card">
      <highcharts
        v-if="showing"
        :options="chartOptions"
        style="border-radius: 15px"
      ></highcharts>
    </div>
    <v-form ref="form" @submit.prevent="onsubmit">
      <v-row style="align-items: baseline">
        <v-col cols="8">
          <v-text-field
            solo
            v-model="unit"
            type="number"
            placeholder="กรอกหน่วยที่ใช้"
          ></v-text-field
        ></v-col>
        <v-col class="mt-5 pl-0 wrapper-btn">
          <v-btn
            block
            elevation="2"
            color="#526FFF"
            style="color: #fff; border-radius: 15px"
            type="submit"
            >บันทึก</v-btn
          >
        </v-col>
      </v-row>
    </v-form>
    <v-row style="margin-top: -30px">
      <v-col>
        <v-simple-table>
          <template v-slot:default>
            <thead>
              <tr>
                <th class="text-left">เดือนที่</th>
                <th class="text-left">หน่วย</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(item, i) in desserts" :key="i">
                <td>{{ i + 1 }}</td>
                <td>{{ item.unit }}</td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
      </v-col>
    </v-row>
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
      unit: 0,
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
          height: this.height - 10,
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
      headers: [
        {
          text: "ลำดับ",
          value: "id",
        },
        { text: "หน่วย", value: "unit" },
      ],
      desserts: [
        {
          id: "Frozen Yogurt",
          unit: 159,
        },
        {
          id: "Ice cream sandwich",
          unit: 237,
        },
      ],
    };
  },
  methods: {
    async onsubmit(){
      console.log("onsubmit");
    }
  }
};
</script>

<style lang="scss" scoped>
</style>

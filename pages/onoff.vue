<template>
  <v-container>
    <div class="wrapper_page">
      <h1 style="color: #ffffff">สถานะไฟฟ้า</h1>
      <v-row class="warpper-input mt-10">
        <b style="padding: 0px 20px">chanel 1</b>
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          ><v-icon dark>{{status ? 'mdi-lightbulb-on' :'mdi-lightbulb'}} </v-icon></v-btn
        >
      </v-row>
      <v-row class="warpper-input mt-10">
        <b style="padding: 0px 20px">chanel 2</b>
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          ><v-icon dark>{{status ? 'mdi-lightbulb-on' :'mdi-lightbulb'}} </v-icon></v-btn
        >
      </v-row>
      <v-row class="warpper-input mt-10">
        <b style="padding: 0px 20px">chanel 3</b>
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          ><v-icon dark>{{status ? 'mdi-lightbulb-on' :'mdi-lightbulb'}} </v-icon></v-btn
        >
      </v-row>
      <v-row class="warpper-input mt-10" @click="status = !status">
        <b style="padding: 0px 20px">chanel 4</b>
        <v-btn elevation="2" fab :class="status ? 'btn-on' : 'btn-off'"
          ><v-icon dark>{{status ? 'mdi-lightbulb-on' :'mdi-lightbulb'}} </v-icon></v-btn
        >
      </v-row>
    </div>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      items: ["1", "2", "3", "4", "5", "6", "7"],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper_page {
  flex-direction: column;
  align-content: center;
  text-align: center;

  .warpper-input {
    align-items: center;
    justify-content: center;
    padding: 0px 20px;
    font-size: 30px;
    b {
      margin: 0;
      color: #fff;
    }

    .btn-on {
      color: #fff;
      background-color: rgb(27, 184, 27) !important;
    }

    .btn-off {
      color: #000;
      background-color: rgba(204, 204, 1) !important;

    }
  }
}
</style>
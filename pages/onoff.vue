<template>
  <div class="wrapper_page">
    <h1>เปิด - ปิดปลั๊กไฟ</h1>
    <v-row class="warpper-input mt-10">
      <v-col cols="2" class="time">
        {{ "00:00" }}
        {{ "00:00" }}
      </v-col>
      <v-select :items="items" label="Solo field" solo></v-select>
      <v-col class="wrapper-btn">
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          @click="status = !status"
          ><v-icon dark> mdi-power-standby </v-icon></v-btn
        >
      </v-col>
    </v-row>
    <v-row class="warpper-input">
      <v-col cols="2" class="time">
        {{ "00:00" }}
        {{ "00:00" }}
      </v-col>
      <v-select :items="items" label="Solo field" solo></v-select>
      <v-col class="wrapper-btn">
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          @click="status = !status"
          ><v-icon dark> mdi-power-standby </v-icon></v-btn
        >
      </v-col>
    </v-row>
    <v-row class="warpper-input">
      <v-col cols="2" class="time">
        {{ "00:00" }}
        {{ "00:00" }}
      </v-col>
      <v-select :items="items" label="Solo field" solo></v-select>
      <v-col class="wrapper-btn">
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          @click="status = !status"
          ><v-icon dark> mdi-power-standby </v-icon></v-btn
        >
      </v-col>
    </v-row>
    <v-row class="warpper-input">
      <v-col cols="2" class="time">
        {{ "00:00" }}
        {{ "00:00" }}
      </v-col>
      <v-select :items="items" label="Solo field" solo></v-select>
      <v-col class="wrapper-btn">
        <v-btn
          elevation="2"
          fab
          :class="status ? 'btn-on' : 'btn-off'"
          @click="status = !status"
          ><v-icon dark> mdi-power-standby </v-icon></v-btn
        >
      </v-col>
    </v-row>
  </div>
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

    .time {
      padding: 0px;
    }
    .wrapper-btn {
      padding: 0px 12px;

      .btn-on {
        color: #fff;
        background-color: rgba(204, 255, 204, 1) !important;
      }

      .btn-off {
        color: #000;
      }
    }
  }
}
</style>
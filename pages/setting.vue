<template>
  <div class="wrapper_page">
    <h1 class="mb-10" style="color: #fff">ข้อมูลการตั้งค่า</h1>
    <v-row
      v-for="(item, index) in items"
      :key="index"
      class="warpper-input"
      style="color: #fff"
    >
      <v-col cols="8" style="text-align: left">
        <p>รูปแบบที่ : {{ item.id }}</p>
        <h1>{{ item.time }}</h1>
        <p>การเปิด : {{ item.day }}</p>
      </v-col>
      <v-col cols="2">
        <v-switch color="success" v-model="item.status" inset></v-switch>
      </v-col>
      <v-col cols="2">
        <v-btn icon color="red" to="/setting_templatetime">
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      items: [
        {
          id: 1,
          time: "10:20",
          day: "อังคาร",
          status: true,
        },
        { id: 2, time: "10:21", day: "จันทร์", status: true },
        { id: 3, time: "10:25", day: "พุธ", status: true },
        { id: 4, time: "10:10", day: "จันทร์", status: true },
        { id: 5, time: "11:10", day: "พุธ", status: true },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper_page {
  align-content: center;
  text-align: center;

  p {
    margin: 0px;
  }

  .warpper-input {
    display: flex;
    flex-direction: row;
    padding: 10px;
    align-items: center;
    border-bottom: 1px solid #c4c4c4;
  }
  i {
    font-size: 40px !important;
  }
}
</style>
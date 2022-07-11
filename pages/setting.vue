<template>
  <div class="wrapper_page">
    <h1 class="mb-10">ข้อมูลการตั้งค่า</h1>
    <v-row v-for="(item, index) in items" :key="index" class="warpper-input">
      <v-col cols="10" style="text-align: left">
        <p>ชื่อรูปแบบ : มหาเพท 1</p>
        <h1>10 : 30</h1>
        <p>การเปิด : ทุกวัน</p>
      </v-col>
      <v-btn icon color="pink">
        <v-icon>mdi-delete</v-icon>
      </v-btn>
    </v-row>
    <v-col class="mt-5 wrapper-btn">
      <v-btn
        block
        large
        :loading="loading"
        :disabled="loading"
        color="primary"
        @click="loader = 'loading'"
      >
        เพิ่มรูปแบบเวลา
      </v-btn>
    </v-col>
  </div>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      items: ["1", "2", "3"],
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
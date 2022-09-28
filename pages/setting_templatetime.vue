<template>
  <div class="wrapper_page">
    <h1 class="mb-10" style="color: #fff">ตั้งค่าเวลาเปิด</h1>
    <v-row class="warpper-input mt-10">
      <v-form>
        <v-row class="warpper-input">
          <v-select
            :items="type"
            item-value="id"
            item-text="name"
            v-model="time.type"
            placeholder="เลือกรูปแบบ"
            solo
          ></v-select>
          <v-select
          v-if="time.type == 1"
            solo
            :items="items"
            v-model="time.day"
            placeholder="วัน"
          ></v-select>
          <v-text-field
            v-if="time.type == 2"
            v-model="time.date"
            solo
            type="date"
            placeholder="วันที่/เดือน/ปี"
          ></v-text-field>
          <v-text-field
            v-model="time.time"
            solo
            type="time"
            placeholder="เวลา HH:MM"
          ></v-text-field>
        </v-row>
        <!-- <v-row
          class="warpper-input my-10"
          style="text-align: center; color: #fff"
        >
          <b style="font-size: 30px">{{ time.time }}</b>
          <b style="font-size: 30px">{{ time.date }}</b>
        </v-row> -->
        <v-col class="mt-5 wrapper-btn">
          <v-btn block large :disabled="loading" color="primary" to="/setting">
            ยืนยัน
          </v-btn>
        </v-col>
      </v-form>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      time: {
        type: null,
        day: null,
        date: "0000/00/00",
        time: "00:00",
      },
      items: [
        "อาทิตย์",
        "จันทร์",
        "อังคาร",
        "พุธ",
        "พฤหัสบดี",
        "ศุกร์",
        "เสาร์",
      ],
      type: [
        { id: 1, name: "รายสัปดาห์" },
        { id: 2, name: "กำหนดเอง" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper_page {
  align-content: center;
  text-align: center;

  .warpper-input {
    display: flex;
    flex-direction: column;
    padding: 10px;
    justify-content: center;
    text-align: left;
  }
  i {
    font-size: 40px !important;
  }
}
</style>
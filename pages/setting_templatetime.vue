<template>
  <div class="wrapper_page">
    <h1 class="mb-10">ตั้งค่าเวลาเปิด</h1>
    <v-row class="warpper-input mt-10">
       <v-form ref="form" @submit.prevent="onsubmit">
        <v-row class="warpper-input">
          <v-select
            :items="type"
            item-value="id"
            item-text="name"
            v-model="time.type"
            placeholder="เลือกรูปแบบ"
            solo
          ></v-select>
          <p v-if="time.type">เวลาเริ่มต้น</p>
          <v-select
            v-if="time.type == 1"
            solo
            :items="items"
            v-model="time.day"
            placeholder="วัน"
          ></v-select>
          <v-text-field
            v-if="time.type == 2"
            v-model="time.strat_tdate"
            solo
            type="date"
            placeholder="วันที่/เดือน/ปี"
          ></v-text-field>
          <v-text-field
            v-if="time.type"
            v-model="time.strat_time"
            solo
            type="time"
            placeholder="เวลา HH:MM"
          ></v-text-field>
          <p v-if="time.type">เวลาสิ้นสุด</p>
          <v-text-field
            v-if="time.type == 2"
            v-model="time.end_date"
            solo
            type="date"
            placeholder="วันที่/เดือน/ปี"
          ></v-text-field>
          <v-text-field
            v-if="time.type"
            v-model="time.end_time"
            solo
            type="time"
            placeholder="เวลา HH:MM"
          ></v-text-field>
        </v-row>
        <v-col class="mt-5 wrapper-btn">
          <v-btn
            block
            elevation="2"
            color="#526FFF"
            style="color: #fff; border-radius: 15px"
            type="submit"
            >บันทึก</v-btn
          >
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
        strat_date: "0000/00/00",
        end_date: "0000/00/00",
        strat_time: "00:00",
        end_time: "00:00",
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
  methods: {
    onsubmit(){
      console.log("onsubmit");
    }
  }
};
</script>

<style lang="scss" scoped>
.wrapper_page {
  align-content: center;

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
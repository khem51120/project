<template>
  <div>
    <v-container>
      <b><h1 class="pt-10 pb-10">หน้าแรก</h1></b>
      <v-row>
        <v-col>
          <div
            class="background drop-shadow1"
            style="
            background-color: #526FFF
              height: 100%;
              align-items: center;
              display: flex;
              justify-content: center;
            "
          >
            <p style="color: #fff; font-size: 75px">0</p>
          </div></v-col
        >
        <v-col>
          <item-menu
            icon="mdi-power-standby"
            title="สถานะการใช้งาน"
            to="onoff"
          ></item-menu>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <item-menu
            icon="mdi-network-strength-4-cog"
            title="ข้อมูลการตั้งค่า"
            to="setting"
          ></item-menu>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <item-menu
            icon="mdi-home-lightning-bolt-outline"
            title="บันทึกหน่วยไฟฟ้า"
            to="saveunit"
          ></item-menu>
        </v-col>
        <v-col> </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style></style>

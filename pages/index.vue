<template>
  <div>
    <v-container>
      <b><h1 class="pt-10 pb-10">หน้าแรก</h1></b>
      <v-row>
        <v-col></v-col>
        <v-col>
          <item-menu icon="mdi-power-standby" title="เปิด - ปิดไฟ"></item-menu>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <item-menu
            icon="mdi-cog-outline"
            title="ตั้งค่าเปิด - ปิด"
          ></item-menu>
        </v-col>
        <v-col>
          <item-menu
            icon="mdi-network-strength-4-cog"
            title="ข้อมูลการตั้งค่า"
          ></item-menu>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <item-menu
            icon="mdi-home-lightning-bolt-outline"
            title="บันทึกหน่วยไฟฟ้า"
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

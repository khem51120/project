<template>
  <v-app>
    <div class="nav">
      <v-container>
        <v-icon> mdi-home </v-icon>
      </v-container>
    </div>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
  .nav {
    text-align: right;
    i{
      font-size: 40px;
    }
    
  }
</style>
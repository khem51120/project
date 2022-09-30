<template>
  <v-app>
    <div class="nav">
      <v-container v-if="this.$route.path != '/'">
        <NuxtLink to="/" style="text-decoration: none;">
          <v-icon style="cursor: pointer; color:#323A5D"> mdi-home-variant-outline </v-icon>
        </NuxtLink>
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
  i {
    font-size: 40px;
  }
}

</style>

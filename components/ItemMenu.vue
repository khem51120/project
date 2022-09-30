<template>
  <div class="background drop-shadow2" @click="$router.push(`/${to}`)">
    <v-icon style="color: #323A5D" size="60" class="pb-2">{{ icon }}</v-icon> <br />
    <b style="font-size: 18px">{{ title }}</b>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    title: String,
    to: String,
  },
};
</script>

<style lang="scss">

.background {
  padding: 20px 20px;
  background-color: #ffffff;
  border-radius: 15px;
  cursor: pointer;
  height: 100%;

}

</style>

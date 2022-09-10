<template>
  <div class="background" @click="$router.push(`/${to}`)">
    <v-icon color="white" size="60" class="pb-2">{{ icon }}</v-icon> <br />
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

<style>
.background {
  padding: 20px 20px;
  background-color: #3b3939;
  border-radius: 10px;
  cursor: pointer;
}

.background b {
  color: rgb(255, 255, 255);
}
</style>

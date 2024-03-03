<template>
  <div id="app">
    <div v-show="isShow">
      <h1>Nguyen tinh</h1>
    </div>
    <button @click="isShow = !isShow">An/Hien</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
    };
  },
  components: {},
};
</script>

<style></style>

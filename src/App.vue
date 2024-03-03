<template>
  <div id="app">
    <div v-show="isShow">
      <h1>Nguyen tinh</h1>
    </div>
    <button @click="isShow = !isShow">An/Hien</button>

    <h1 :class="{ daChon: selected, abc: xyz }">Nguyen Tinh 2</h1>
    <button @click="selected = !selected">Click</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
      selected: true,
    };
  },
  components: {},
};
</script>

<style>
.daChon {
  color: red;
}
</style>

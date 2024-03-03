<template>
  <div id="app">
    <div v-show="isShow">
      <h1>Nguyen tinh</h1>
    </div>
    <button @click="isShow = !isShow">An/Hien</button>

    <h1 :class="{ daChon: selected, abc: xyz }">Nguyen Tinh 2</h1>
    <button @click="selected = !selected">Click</button>
    <todoList />
  </div>
</template>
<script>
import todoList from "./components/todoList.vue";
export default {
  data() {
    return {
      isShow: true,
      selected: true,
    };
  },
  components: { todoList },
};
</script>

<style>
.daChon {
  color: red;
}
</style>

<template>
  <div class="list">
    <div
      v-for="(language, index) in languages"
      :key="index"
      @click="language.selected = !language.selected"
      :class="{ selected: language.selected }"
    >
      <span>{{ language.name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [
        { name: "English", selected: false },
        { name: "English1", selected: false },
        { name: "English2", selected: false },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.list div {
  display: inline-block;
  border: 1px solid #ebebeb;
  padding: 4px 15px;
  margin-right: 5px;
  border-radius: 4px;
}
.list div.selected {
  background-color: green;
  color: white;
}
</style>

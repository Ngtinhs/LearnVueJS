<template>
  <div class="todoList">
    <!-- <input type="text" v-model="newTask" />
    <button @click="addTask()">Them</button> -->
    <!-- <div v-for="(task, index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done" />
      <span :class="{ done: task.done }">{{ task.content }}</span>
    </div> -->
    <taskData v-for="(task, index) in tasks" :key="index" :taskDataa="task" />
  </div>
</template>
<script>
import taskData from "./taskData.vue";
export default {
  data() {
    return {
      newTask: "",
      tasks: [
        { content: "aaa", done: false },
        { content: "b", done: false },
        { content: "c", done: false },
      ],
    };
  },
  mounted() {},

  methods: {
    addTask: function () {
      this.tasks.push({ content: this.newTask, done: false });
    },
  },
  watch: {
    newTask: function (newValue, oldValue) {
      console.log(newValue);
      console.log(oldValue);
    },
  },
  components: { taskData },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.done {
  text-decoration: line-through;
}
</style>

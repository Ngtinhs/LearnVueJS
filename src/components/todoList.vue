<template>
  <div class="todoList">
    <input type="text" v-model="newTask" />
    <button @click="addTask()">Them</button>
    <div v-for="(task, index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done" />
      <span :class="{ done: task.done }">{{ task.content }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: "",
      tasks: [
        { content: "a", done: false },
        { content: "b", done: false },
        { content: "c", done: false },
      ],
    };
  },
  methods: {
    addTask: function () {
      this.tasks.push({ content: this.newTask, done: false });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.done {
  text-decoration: line-through;
}
</style>

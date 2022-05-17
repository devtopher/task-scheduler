<template>
  <MyHeader />
  <div class="wrapper">
    <TaskModule @module-close-event="toggleModule" v-if="newTask" />
    <ScheduleGrid :taskMapFromParent="taskMap" />
    <MyButton buttonText=" New Task" @click="openModule" />
  </div>
</template>

<script>
import MyButton from "./components/MyButton";
import MyHeader from "./components/MyHeader";
import ScheduleGrid from "./components/ScheduleGrid.vue";
import TaskModule from "./components/TaskModule.vue";
export default {
  name: "App",
  components: {
    MyHeader,
    ScheduleGrid,
    MyButton,
    TaskModule,
  },
  data() {
    return {
      taskMap: {
        testKey: "",
        eleven: "",
        twelve: "",
        thirteen: "",
        fourteen: "",
        fifteen: "",
        sixteen: "",
        seventeen: "",
        eighteen: "",
      },
      newTask: false,
      selectedHour: 0,
      selectedMessage: "",
    };
  },
  methods: {
    toggleModule: function (value) {
      let key = value.selectedHour;
      this.taskMap[key] = value.selectedMessage;
      this.newTask = !this.newTask;
    },
    openModule: function () {
      this.newTask = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 2em;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>

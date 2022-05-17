<template>
  <Header />
  
  <div class="wrapper">
    <TaskModule v-if="newTask" />
    <ScheduleGrid />
  <Button buttonText="New Task" @click="addTask"/>
  </div>
  

</template>

<script>
import Button from './components/Button'
import Header from './components/Header'
import ScheduleGrid from './components/ScheduleGrid.vue'
import TaskModule from './components/TaskModule.vue'
export default {
  name: 'App',
  components: {
    Header,
    ScheduleGrid,
    Button,
    TaskModule
  },
  data(){
    return{
      newTask: false,
      
    }
  },
  methods:{
    addTask(){
      this.newTask = !this.newTask
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
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

<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="task in tasks" v-bind:key="task.id"> {{ task.title }} </li>
    </ul>
    <form action="" @submit.prevent="addNewTask">
      <input type="text">
      <button>Add task</button>
    </form>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HelloWorld
  },
  data: function () {
    return {
      msg: "Task list",
      tasks: [
        {id:1, title: "Get up"},
        {id:2, title: "Never give up"},
        {id:3, title: "Victory"},
      ]
    }
  },
  methods:{
    addNewTask(e){
      console.log(e.target[0].value);
      this.tasks.push({id:this.tasks.length +1, title: e.target[0].value})
    }
  }
}
</script>

<style>

</style>

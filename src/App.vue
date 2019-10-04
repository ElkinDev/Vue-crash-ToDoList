<template>
  <div id="app">
    <Todos v-bind:todos="todos"/>
  </div>
</template>

<script>

  import Todos from './components/Todos'

export default {
  name: 'app',
  components: {
    Todos
  },
  data(){
    return{
      todos:[
      {
        id:2,
        title:"To-do one",
        completed:false
      },
      {
        id:1,
        title:"To-do Second",
        completed:true
      },
      {
        id:3,
        title:"To-do third",
        completed:false
      },
      {
        id:4,
        title:"To-do Fourth",
        completed:true
      },
      {
        id:5,
        title:"To-do fifth",
        completed:false
      },
      {
        id:6,
        title:"To-do sixth",
        completed:true
      }

      ]
    }
  }
}
</script>

<style>

</style>

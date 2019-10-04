<template>
  <div id="app">
    <HeaderLayout/>
    <AddTodo v-on:add-todo="addTodo"/>

    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
  import HeaderLayout from './components/layout/Header1'; 
  import Todos from './components/Todos';
  import AddTodo from './components/AddTodo'
export default {
  name: 'app',
  components: {
    Todos,
    HeaderLayout,AddTodo
  },
  data(){
    return{
      todos:[
      {
        id:1,
        title:"To-do one",
        completed:false
      },
      {
        id:2,
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
  },
  methods:{
    deleteTodo(idItem){
      this.todos=this.todos.filter(todo=>todo.id !==idItem)
    },
    addTodo(newTodo){
      this.todos=[...this.todos,newTodo]
    }
  }
}
</script>

<style>
@charset "UTF-8";

*{ 
    outline:0 !important;
    box-sizing: border-box;
    margin:0;padding:0;

}
.c-while{
    color:#fff !important;
}
body {
    font-family: Arial, Helvetica, sans-serif;
    position: relative;
}

a {
    color: #5a7392;
}

h1 {
    font-size: 60px;
    font-weight: 300;
    letter-spacing: -1px;
    margin-bottom: 0.2rem;
}

h2 {
    font-size: 45px;
    font-weight: 300;
    letter-spacing: -1px;
    margin-bottom: 1rem;
}

h3 {
    font-size: 33px;
    font-weight: 500;
}

h4 {
    font-size: 20px;
    font-weight: 400;
}

h5 {
    font-size: 28px;
    font-weight: 300;
    margin-bottom: 0.7rem;
}

p {
    color: #b8c0cb;
}
.btn{
  display: inline-block;
  border:none;
  background:#555;
  color:#fff;
  padding: 7px 20px;
  cursor: pointer;
}
.btn:hover{
  background: #666;
}
</style>

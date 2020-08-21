<template>
<!-- We can only have one div in template -->
  <div >
    <Header logo="JAMCo" />
    <h1 class="headerText">Hello World, my name is {{name}}, I'm {{age}} this year.</h1>
    <Todo v-bind:lists="todos"/>
    <Footer abc="abcd"/>
  </div>
</template>

<script>
//import component
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Todo from "./components/Todo.vue";

export default {
  name: 'App',
  components: {
    Header, Footer, Todo
  },
  data() {
    return{
      name: 'jam',
      gender: 'male',
      age: 20,
      todos:[
        {
          id:1,
          title: "task 1",
          completed: false,
        },
        {
          id:2,
          title: "task 2",
          completed: true,
        },
        {
          id:3,
          title: "task 3",
          completed: false,
        }
        
      ]
    }
  }
}
</script>

<style>

*{
  margin:0;
  padding: 0;
  box-sizing: border-box;
  }




</style>


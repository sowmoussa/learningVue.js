<template>
  <div id="app">
   <todos v-model="todos"></todos>
   <button @click.prevent="addTodo">Ajouter</button>
  </div>
</template>

<script>
import Todos from './components/Todos'

export default {
  data(){
    return {
      todos: [{
        name:'Démo',
        completed: true
      }]
    }
  },
  methods:{
    addTodo(){
      this.todos.push({
        name:'Jean',
        completed: false
      })
    }
  }, 
  components:{
    Todos
  }
}
</script>


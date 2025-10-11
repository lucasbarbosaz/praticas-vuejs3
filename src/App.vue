<template>
  <div>
    <h1>{{ fullName }}</h1> <br>

    <h2>Todos em aberto</h2>
    <div v-for="todo in unCompletedTodos" :key="todo.id">
      <p>
        <strong>{{ todo.title }}</strong>
      </p>
    </div>
    <br>
    <h2>Todos concluídos</h2>
    <div v-for="todo in completedTodos" :key="todo.id">
      <p>
        <strong>{{ todo.title }}</strong>
      </p>
    </div>
    <br><br><br>
    <h2>Todos</h2>
    <div v-for="todo in todos" :key="todo.id">
      <input type="checkbox" v-model="todo.completed"/>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data: () => {
    return {
      user: {
        firstName: 'John',
        lastName: 'Snow'
      },
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }
  },

  computed: {
    fullName() {
      return `${this.user.firstName} ${this.user.lastName}`
    },

    unCompletedTodos() {
      return this.todos.filter(todo => !todo.completed)
    },

    completedTodos() {
      return this.todos.filter(todo => todo.completed)
    }
  },

  methods: {
  },
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
</style>

<template>
  <div>
    <button @click.once="onClick">
      Enviar
    </button>
    <br><br>

    <div @mouseover.once="onMouseOver" @mouseout.once="onMouseOut">
      Passe o mouse aqui
    </div>

    <br><br>
    <form action="https://google.com" @submit.prevent="onSubmit">
      <input type="text" @keyup.enter="onKeyUp" />
    </form>
  </div>
</template>

<script>


export default {
  name: 'App',
  data: () => {
    return {
      var: 'teste'
    }
  },
  methods: {
    onClick($evt) {
      console.log('Clicou', $evt)
    },

    onMouseOver($evt) {
      console.log('Passou o mouse', $evt)
    },

    onMouseOut($evt) {
      console.log('Tirou o mouse', $evt)
    },

    onSubmit($evt) {
      console.log('Enviou o form', $evt)
    },

    onKeyUp($evt) {
      console.log('Soltou a tecla', $evt)
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
</style>

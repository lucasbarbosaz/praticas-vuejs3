<template>
  <div>
    <div>
      Two way data binding
      v-model -> formularios
    </div>

    <br><br>

    <div>
      <label for="name">Name: </label>
      <input v-model="name" type="text" placeholder="Enter your name" /> <br><br>
      {{ name }}
    </div>

    <br /><br />

    <div>
      <label for="sports">Choose a sport: </label>
      <select v-model="sports">
        <option disabled value="">Please select one</option>
        <option value="football">Football</option>
        <option value="basketball">Basketball</option>
        <option value="tennis">Tennis</option>
      </select> <br><br>
      {{ sports }}
    </div>
    <br /><br />
    <div>
      <label>Newsletter Subscription: </label>
      <input v-model="newsletter" type="radio" value="Sim" /> Sim
      <input v-model="newsletter" type="radio" value="Não" /> Não
      <br><br>
      {{ newsletter }}
    </div>

    <br /><br />
    <div>
      <label>Contrato</label>
      <input v-model="contract" type="checkbox" /> Aceita nossos termos
      <br><br>
      {{ contract }}
    </div>


    <br /><br />
    <div>
      <label>Cores que você mais gosta </label>
      <input v-model="colors" type="checkbox" value="Vermelho" /> Vermelho
      <input v-model="colors" type="checkbox" value="Verde" /> Verde
      <input v-model="colors" type="checkbox" value="Azul" /> Azul
      <br><br>
      {{ colors }}
    </div>
  </div>

</template>

<script>


export default {
  name: 'App',
  data: () => {
    return {
      name: '',
      sports: '',
      newsletter: '',
      contract: false,
      colors: []
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

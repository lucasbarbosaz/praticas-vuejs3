<template>
  <div>



    <div v-for="(obj, index) in array" v-bind:key="obj.id" class="item">
      {{ index }}. {{ obj.name }}
    </div>


    
  </div>

</template>

<script>


export default {
  name: 'App',
  data: () => {
    return {
      array: [
        { id: 1, name: 'Item 1' },
        { id: 2, name: 'Item 2' },
        { id: 3, name: 'Item 3' },
        { id: 4, name: 'Item 4' },
        { id: 5, name: 'Item 5' }
      ]
    }
  }
}
</script>

<style>
.item {
  margin: 10px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #f9f9f9;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div>

    <h1 :class="{ 'title': true, 'text-home': isHome }">Vue.js 3</h1>

    <p :class="pClass">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus, corrupti cumque minus laborum commodi possimus ipsum provident ipsa sint modi, libero est? Consequatur ipsam non voluptates et sint rerum reprehenderit.
    </p>

    <p :style="styleClass">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi quidem iste quam aperiam illum tempora perspiciatis soluta mollitia ipsam quo voluptatem, accusantium magni ratione, vel non quae nisi fugiat aliquam.
    </p>

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
      isHome: true,
      classVar: 'title',
      pClass: ['text', 'text-home'],
      title: 'Aprendizagem Vue.js',
      styleClass: { 'color': 'aqua', backgroundColor: 'black' },
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
.text-home {
  font-size: 48px;
  color: #35495e;
}

.title {
  color: #42b983;
  font-size: 32px;
}

.text {
  color: gray;
}

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

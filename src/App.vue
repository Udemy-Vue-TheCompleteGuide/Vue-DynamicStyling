<template>
  <div id="app">
    <Styling></Styling>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Styling from "@/components/Styling";

export default {
  name: 'App',
  components: {
    Styling,

    // eslint-disable-next-line vue/no-unused-components
    HelloWorld
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

* {
  box-sizing: border-box;
}

html {
  font-family: 'Jost', sans-serif;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: #4fc08d;
  color: white;
  text-align: center;
}

#styling {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

.demo {
  width: calc(100% - 32px);
  height: 100px;
  margin: 16px;
  border: 2px dashed #ccc;

  display: flex;
  justify-content: center;
  align-items: center;
}

.active {
  border-color: red;
  background-color: salmon;
}
</style>

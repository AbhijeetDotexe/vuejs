<template>
  <h1>{{ test }}</h1>
  <ChildComponent></ChildComponent>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ChildComponent from './components/ChildComponent.vue';

export default {
  name: 'App',
  components: {
    ChildComponent,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  height: 100vh;
  /* margin-top: 60px; */
  border: 2px solid black;
  border-radius: 14px;
  background-color: #212121;
  display: flex;
  justify-content: center;
}
</style>

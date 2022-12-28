<template>
  <div>
    My name is {{name}} and I am {{ age }}  years young.
    <div v-text="channel"></div>
  </div>
  
</template>
<script>
export default {
  name: 'App',
  data(){
    return {
      name: "Peter",
      age: "29",
      channel: "codeInvasion",
    };
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

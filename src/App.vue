<template>
 <template v-for="name in names" :key="name">
  <h2 v-if="name === 'bruce'">{{ name }}</h2>
  
  </template>
  <h2>Add method - {{ add(10,15,20) }}</h2>
  <h2>Multiply method - {{ multiply(10) }}</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      baseMultplier: 5,
      names: ['bruce','clark','diana'],
    }
  },

  methods: {
    add(a,b,c){
      return a +b +c

    },
    multiply(num){
      return num*this.baseMultplier
    }
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

.underline{
  text-decoration: underline;
}

.promoted{
  font-style: italic;
}

.new{
  color: olivedrab;
}

.sold-out{
  color: red;
}
</style>

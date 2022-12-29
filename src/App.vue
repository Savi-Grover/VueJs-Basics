<template>
<h2>{{ name }}</h2>
<div><button @click="changename($event),increment($event)" >Change name</button>
</div>

<h2>{{ count }}</h2>


  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      name: 'Savi',
      count: 0
    }
  },

  methods: {
    increment(){
      return this.count +=1;
    },

    decrement(){
      return this.count -=1;
    },

    changename(){
      this.name= 'Batman'
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

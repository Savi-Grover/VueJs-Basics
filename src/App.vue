<template>
  <div>
    My name is {{name}} and I am {{ age }}  years young.
    <div v-text="channel"></div>
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">checkButton</button>
    <h2 class="underline">Under lined text from style class</h2>
    <h2 v-bind:class="Status">Status</h2>
    <h2 class="underline" v-bind:class="Status">2 classes</h2>
    <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
    <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">Sold out/new</h2>
    <h2 v-bind:class="['new','promoted']" >2 classes </h2>
    <h2 v-bind:class="[isPromoted && 'promoted',isSoldout ? 'sold-out': 'new']" >Conditional Array</h2>
    <h2 v-bind:class="{
      promoted : isPromoted,
      new : !isSoldout,
      'sold-out': isSoldout
     }">object conditional classes</h2>

    <h2 v-bind:style="{
      color: highlightedcolor,
      'font-size': headersize +'px'
    }">Inline style</h2>

    <h2 v-bind:style="headerstyleobject">Calling headerstyle object data </h2>
    <h2 v-bind:style="[baseStyle,successStyle]">Array  object data </h2>
  </div>
  
</template>
<script>
export default {
  name: 'App',
  data(){
    return {
      name: "Peter",
      age: "29",
      headingId: '3',
      isDisabled: true,
      Status:"danger",
      isPromoted: true,
      isSoldout:true,
      isNew: true,
      highlightedcolor: 'orange',
      headersize: 120,
      headerstyleobject: {
        color: 'green',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyle:{
        color: 'green',
        fontSize: '55px'
      },
      successStyle:{
        padding: '12px'
      },
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

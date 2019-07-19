<template>
  <div id="app">
    <span>{{text}}</span><br>
    <button @click="add">点我+</button>
    <button @click="sub">点我-</button>
  </div>
</template>

<script>
import { METHODS } from 'http';
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data:function(){
    return{
      count: 0,
      text:""
    };
  },
  methods:{
    add:function(){
     this.count++;
     this.text="add a number: "+this.count
    },
    sub:function(){
     this.count--;
     this.text="sub a number: "+this.count
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

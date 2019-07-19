<template>
  <div id="app">
    请输入：<input type="text" v-model="counter"><br>
    <counter-sum :counter="counter"></counter-sum>
  </div>
</template>

<script>
//import { METHODS } from 'http';
import CounterSum from './components/CounterSum.vue';

export default {
  name: 'app',
  data:function(){
    return{
      counter:10
    };
  },
  components: {
    CounterSum
  }
}
</script>


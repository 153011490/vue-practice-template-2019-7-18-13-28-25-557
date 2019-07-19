<template>
  <div>
    <div v-for="index in parseInt(counter)" :key="index">
      <CounterGroup ref="CounterGroup" @calculate="calculate"></CounterGroup>
    </div>
    <div>
        总计:{{sum}}
    </div>
  </div>
</template>

<script>

import CounterGroup from './CounterGroup';

export default {
  name: 'CounterSum',
  props:['counter'],
  components:{
      CounterGroup
  },
  data:function(){
      return{
          sum:0
      }
  },
  methods:{
      calculate:function(params) {
          this.sum+=params;
      }
  }
}
</script>


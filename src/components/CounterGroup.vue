<template>
  <div>
    <span>{{count}}</span><br>
    <button @click="add">点我+</button>
    <button @click="sub">点我-</button>
  </div>
</template>

<script>
export default {
  name: 'CounterGroup',
  data:function(){
    return{
      count: 0
    };
  },
  props:['sum'],
  methods:{
    add:function(){
     this.count++;
     this.$emit('calculate',1);
    },
    sub:function(){
     this.count--;
     this.$emit('calculate',-1);
    }
  }
}
</script>


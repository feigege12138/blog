<template>
  <div>
    <div v-for="(item,index) in list" :key="index">{{item}}</div>
  </div>
</template>

<script>
export default {
  props:["list"],
  data(){
    return{
    }
  },
  created(){
  },
  mounted(){
  }
}
</script>

<style>
.aaa{
  width: 100px;
  height: 300px;
  background-color: red;
}
</style>
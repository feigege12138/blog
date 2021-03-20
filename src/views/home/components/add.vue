<template>
  <div>
    <input type="text" v-model="text">
    <button @click="add()">点击添加</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      text:'123123123123123'
    }
  },
  methods:{
    add(){
      this.$emit('add', this.text)
    }
  },
  created(){
    this.$emit('add',this.text)
  }
}
</script>

<style>

</style>
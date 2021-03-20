<template>
  <div>
    123
  </div>
</template>

<script>

const fs = require ('fs')
console.log(fs)

let p = new Promise((resolve,reject)=>{
 fs.readFile('./text.txt',(err,data)=>{
   if(err){
     reject(err)
   }else{
     resolve(data)
   }
 })
})

// p.then(value=>{
//   console.log(value)
// },error=>{
//   console.log(error)
// })
</script>

<style>

</style>
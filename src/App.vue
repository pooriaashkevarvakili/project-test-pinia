<script>
import HelloWorld from  "./components/HelloWorld.vue"
import {counterStore}from "./store/counter"
export default {
  components:{
    HelloWorld
  },
  setup(){
const store=counterStore()
    return{
  store
    }
  }
}
</script>

<template>
 <div class="flex flex-col items-center justify-center">
   <button class="bg-red-500 text-3xl mt-10 text-white rounded-full w-5/12" @click="store.addCount()">
     {{store.counter}}
   </button>
   <button @click="store.$reset">reset</button>
 </div>
</template>

<style>

</style>

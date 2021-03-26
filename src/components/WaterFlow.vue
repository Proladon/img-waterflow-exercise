<template>
  This is Water Flow
  <!-- {{img.source}} -->
  <img v-for="img in img.source" :key="img" :src="img" alt="">
  <!-- <img :src="a" alt=""> -->
</template>

<script setup>
import { onMounted, reactive } from "vue";

// all img file path
const img = reactive({
    source:[]
})

onMounted(()=>{
    
    // get all img file path & store in img.source
    for(let num=1; num<13; num++){
        let filePath = `/src/assets/img (${num}).jpg`
        img.source.push(filePath)
    }

})

</script>

<style>
</style>
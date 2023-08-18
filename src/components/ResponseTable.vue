<script setup>
import { ref } from "vue";

//偵測解析度
const currentWindorWidth = window.innerWidth;
console.log(currentWindorWidth);
const mode = ref('desktop');
if(currentWindorWidth > 764){
  console.log('桌機');
  mode.value = 'desktop';
}else{
  console.log('行動裝置');
  mode.value = 'mobile';
}


</script>

<template>
測試
</template>

<style scoped>

</style>
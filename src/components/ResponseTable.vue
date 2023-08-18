<script setup>
import { ref, onMounted, onUnmounted } from "vue";

//偵測解析度
const currentWindorWidth = ref(null);
const mode = ref('desktop');

const handleResize = () => {
    currentWindorWidth.value = window.innerWidth
    if(currentWindorWidth < 764){
      mode.value = 'mobile';
    }else{
      mode.value = 'desktop';
    }
    console.log(currentWindorWidth.value);
}

onMounted(() => {
    window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
    window.removeEventListener('resize', handleResize)
})
</script>

<template>
  <div v-if="mode == 'desktop'">
    桌機模式
  </div>
  <div v-if="mode == 'mobile'">
    行動模式
  </div>
</template>

<style scoped>

</style>
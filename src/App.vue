<script lang="ts">
  
  import Banner from './components/Banner.vue'
  import ConteudoPrincipal from './components/ConteudoPrincipal.vue'
  import setupHook from './hook/setupHook.vue';
     
  export default {
    components: { Banner, ConteudoPrincipal, setupHook }    
  }  
</script>

<template>
  <Banner />
  <ConteudoPrincipal />    
  <setupHook />
</template>

<style scoped></style>
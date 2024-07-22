<script lang="ts">
  
  import Banner from './components/Banner.vue'
  import ConteudoPrincipal from './components/ConteudoPrincipal.vue'
  import desmontagemHook from './hook/desmontagemHook.vue'
     
  export default {
    components: { Banner, ConteudoPrincipal }    
  }  
</script>

<template>
  <Banner />
  <ConteudoPrincipal />  
  <desmontagemHook />
</template>

<style scoped></style>
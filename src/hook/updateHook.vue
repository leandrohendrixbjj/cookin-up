<script lang="ts"> 
/*
    [beforeUpdate] => entra em execução imediatamente após uma propriedade reativa ser alterada, 
    mas imediatamente antes do componente ser re-renderizado em tela.
    Muito utilizado para operações de debugging para identificar em que momento a renderização do componente é ativada.
    
    [mounted] => O mounted é executado imediatamente após o componente ser montado. Nesse estágio, o componente se 
    torna funcional: as propriedades de data() são injetadas no template, os elementos são renderizados e a 
    manipulação do DOM se torna possível. 
*/    
   
export default {    
  data() {
    return { 
      contador: 0,
      historico: []
    }
  },
  beforeUpdate(){ 
    alert("Welcome to BeforeUpdate")           
  },  
  mounted() {       
    this.contador++      
  },
}  
</script>

<template>  
   <h1>Contador: {{ contador }}</h1> 
</template>

<style scoped>  
</style>
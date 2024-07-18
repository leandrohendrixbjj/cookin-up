<script lang="ts"> 
/*
    [beforeUpdate] => entra em execução imediatamente após uma propriedade reativa ser alterada, 
    mas imediatamente antes do componente ser re-renderizado em tela.
    Muito utilizado para operações de debugging para identificar em que momento a renderização do componente é ativada.

    [updated] =>  é executado imediatamente após uma re-renderização do componente causado por uma alteração de 
    dados reativos, sendo bastante útil para criação de efeitos colaterais (side effects) relacionados ao DOM.
    
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
    alert("Welcome to BEFORE UPDATE")           
  },  
  updated() {
    alert("Welcome to UPDATE")    
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
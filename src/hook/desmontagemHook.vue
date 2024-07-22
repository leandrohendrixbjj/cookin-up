<script lang="ts"> 
/*
    Os hooks de desmontagem, também chamados de destruction hooks são executados imediatamente 
    antes ou depois de um componente ser desmontado.
    
    [ beforeUnmount ] é executado imediatamente antes do componente ser desmontado. 
    É importante ressaltar que, nesse ponto, o componente ainda está totalmente funcional, 
    então é uma ótima etapa para executar funções de clean up, como remoção de event listeners, 
    exclusão de variáveis, ações de logout, etc.
    
*/    
   
export default {    
  data() {
    return {
      contador: 0
    };
  },
  mounted() {       
    this.contador++      
  },
  beforeUnmount() {
   alert("Welcome to BEFORE UNMOUNT")          
  }  
}  
</script>

<style scoped>  
</style>
<!-- 
  [ setup ] => é uma parte essencial da Composition API, que é uma abordagem mais flexível, funcional e modular para a 
               criação de componentes em comparação com a sintaxe do Vue 2. Ele é usado para configurar e inicializar o 
               estado, props, métodos e outras opções de um componente Vue. No entanto, apesar de ser uma feature 
               da Composition API, é totalmente possível utilizar o setup() dentro da Options API como facilitador para 
               seu código. Veja como fica a sintaxe do hook em ambos os casos:
-->
<script lang="ts"> 
  export default {    
    setup () {
      alert("Setup com Options API")
    }
  }  
</script>

<!-- OR 
<script setup>
  alert("Setup com Composition API")
</script>
--> 
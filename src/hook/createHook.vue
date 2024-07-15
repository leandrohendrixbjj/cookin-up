<script lang="ts">
  /* 
    [beforeCreate] => é executado imediatamente assim que um componente é inicializado. 
    Nesse momento, estados e propriedades computadas ainda não foram processadas.
    Esse hook é bastante útil, por exemplo, para realizar uma solicitação de autenticação. 
    Permitindo que você lide com a autenticação antes que qualquer conteúdo seja exibido na tela.

    [created] => também é executado antes do componente ser montado no DOM porém, nessa etapa todos 
    os estados, propriedades computadas, métodos e watchers já foram processados e estão prontos para 
    serem acessados;
    Esse é um hook muito útil para fazer uma requisição HTTP para uma API e atualizar o estado do componente 
    com esses dados, que serão renderizados no DOM.

    [beforeMount] => semelhante ao created, sendo a principal diferença o momento em que ambos são executados:

        created: é acionado após a criação do componente e permite acesso às opções de dados, 
        mas antes que o DOM seja montado.

        beforeMount: é acionado imediatamente antes da montagem do DOM, logo depois de uma pré-compilação do template 
        e do style do componente.

    [mounted] => O mounted é executado imediatamente após o componente ser montado. Nesse estágio, o componente se 
    torna funcional: as propriedades de data() são injetadas no template, os elementos são renderizados e a 
    manipulação do DOM se torna possível.    
  */
   
  export default {    
    data() {
      return { 
        message: 'Welcome to Cooking',
        items: [{ id: 1, name: 'Item 1' }] 
      }
    }, 

    beforeCreate() {
      alert('beforeCreate foi chamado')
    },
    
    created() {
      alert(this.message)
    },
    
    beforeMount() {
    // Simulando o retorno de uma API
    setTimeout(() => {
    alert('beforeMount foi chamado')
    }, 2000)
  },
  
  mounted() {
    const listItems = this.items
    listItems.forEach((item) => {
      alert(`Você está no item: ${item.name}`)    
    })
  }
}  
</script>

<template>  
</template>

<style scoped></style>
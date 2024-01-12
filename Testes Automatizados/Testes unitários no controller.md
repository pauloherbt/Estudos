# Introdução
Para realizar testes unitários no controller/resources de nossa aplicação, utilizando SpringFramework em conjunto com Mockito framework, temos algumas annotations para facilitar nosso trabalho.
## @WebMvcTest(ControllerClass.class)
Responsável por indicar o contexto que irá ser carregado para nossa classe de Testes. Essa annotation carrega apenas o contexto necessário para realizar requisições que serão interceptadas pelo nosso controller, além de classes auxiliares como um tratador de exceções.
## Utilizando @MockBean
Quando a classe a ser mockada é um Bean do Spring, para melhor integração com o ambiente utilizamos a classe MockBean que faz parte do pacote**org.springframework.boot.test**. 
Ela nos permite realizar as mesmas funções e simular comportamentos da classe [Mockito](Mockito.md).
> Lembrete: Sempre defina o comportamento dos métodos do objeto mockado.
## Classes Auxiliares
### MockMvc
Nos permite criar um objeto para performar requisições de forma fácil e customizável, tais requisições serão interceptadas pelo nosso controller e podemos realizar a assertion do teste no próprio objeto mockMvc, por meio do método ``andExpect()``.
### MockMvcRequestBuilder
É uma classe utilitária na qual podemos especificar parâmetros de uma requisição de forma simplificada.
Nos disponibiliza vários métodos HTTP ja implementados como métodos da referida classe, utilizaremos para especificar o metodo da requisição no MockMvc.
### MockMvcResultMatchers
É uma classe utilitária que contém métodos no qual podemos colher informações sobre a resposta da requisição que foi executada. O mais comum é utilizar para verificar se o código HTTP retornado pela requisição era o que nós esperávamos. 
### Exemplo de uma requisição com mockMvc
Ao deleter um product com id existente, nossa api deve retornar o código HTTP 204 NO CONTENT, é o que verificamos no Teste abaixo.
```java
@Test  
void deleteShouldReturnNoContentWhenIdExists() throws Exception {  
    //configurando o comportamento do metodo
    doNothing().when(productService).deleteById(existingId);
    //fazendo a requisicao e o assertion da resposta esperada  
    mockMvc.perform(delete("/products/{id}",existingId))
    .andExpect(status().isNoContent());  
}
```

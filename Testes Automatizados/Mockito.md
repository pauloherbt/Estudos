<-[Testes em java](Testes%20em%20java.md)
# Introdução
É um framework para testes **unitários** com o objetivo de instanciar classes e controlar o comportamento dos métodos.
![](../img/mockscheme.png)

Simula o comportamento de uma classe, sem executar a ação do verdadeiro método.
Isso é importante para, **testar a unidade.** Pois conseguimos isolar o comportamento de um metodo, por isso são chamados de testes unitários.
## Funcionalidades
### Mock:
Cria uma instância de uma classe, de forma _mockada_ não irá chamar o método real, ao menos que queira.
Ao criar o Mock, o programador não pode esquecer de configurar o comportamento dele.
### InjectMocks
Cria uma instância e injeta as dependências necessárias que estão anotadas com _@Mock._
### Verify
Permite verificar a quantidade de vezes que foi executado um método, ou uma sequência de ações e com os parâmetros corretos.
### When
Utilizado para configurar o comportamento do mock, pode direcionar o retorno do método, dado um parâmetro de entrada.
> bom para simular métodos com retorno.
> Quando o método é void, use `doSomething*( )`

## Mock vs MockBean
**MockBean** faz parte do pacote Spring, é útil para escrever testes de integração, quando se quer mockar algum _bean_ do sistema, pois carrega todo o contexto da aplicação.
>É usado com: 
>@SpringBootTest e @WebMvcTest
   Exemplo: mockando um service, para [Testes unitários no controller](Testes%20unitários%20no%20controller.md)
   
**Mock** faz parte do pacote vanilla do mockito, e é uma forma mais rápida de mockar uma classe. É mais rápido e enxuto.
>É usado com @ExtendWith(), quando a classe não carrega o contexto da aplicação, outras camadas, ideal para testes unitários.


Utilizamos a biblioteca JUnit 5
## Processo AAA
### Boas Práticas
1. Utilizar o padrão factory para criação dos objetos a serem testados.Atua como uma classe com métodos auxiliares, podemos ter diferentes formas de instancia-lo.
## Annotation do junit vanilla
+ @Test -> acompanha cada método
+ @Assertions.assert.. -> realiza a verificação de alguma condição pra validar o teste
+ @BeforeEach -> executa o que está no bloco de codigo, geralmente um método setup, sempre antes de rodar um teste
## Annotations utilizando SpringBoot
+ @SpringBootTest -> carrega o contexto da aplicação, ideal para testes de integração, mas torna os testes unitários lentos.
+ @SpringBootTest
	+ @AutoConfigureMockMvc -> carrega o contexto da aplicação, trata as requisições sem subir o servidor. (teste de integração e web)
+ @WebMvcTest(Classe.class) -> carrega apenas o contexto necessário da camada web. (testar um controller)
+ @ExtendWith(SpringExtension.class) -> não carrega o contexto, permite usar os recursos do Spring+ JUnit (testes de unidade de forma leve, service/component)
+ @DataJpaTest -> carrega somente os componentes necessários para o Spring Data JPA, Cada teste é transactional e retorna para o seu estado original(rollback), bom pra teste de unidade do repository
### Fixtures
É uma forma de organizar o código e evitar repetições.
+ @BeforeAll -> preparação antes de todos os testes
+ @AfterAll -> dps de todos
+ BeforeEach -> execcuta antes de cada um
+ AfterEach -> dps de cada um
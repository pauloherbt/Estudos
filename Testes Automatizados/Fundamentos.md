Testes automatizados verificam se uma parte específica do código  se comporta da forma que deveria. 
Garante uma maior segurança do código, é vantajoso para a construção de grandes aplicações, na qual futuramente será composta de tantas funcionalidades que se tornará impossível testar manualmente.
## Tipos de Testes
### Testes Unitários
São os testes realizados na menor unidade testável de um programa, por exemplo: o comportamento de métodos de uma classe. O teste unitário não acessa recursos externos.
### Testes de Integração
Focado em verificar a comunicação entre componentes/módulos da aplicação, os recursos externos, interação entre camadas(ex: service, repository,resource).
### Teste de Funcionalidade
Teste do ponto de vista do usuário, verifica se determinada funcionalidade executa o comportamento esperado pelo usuário. Casos de uso: interação usuário-sistema.
## Vantagens
- Detectar se a implementação de novas features violaram as regras do sistema
- É uma forma de documentação, o teste fornece a entrada e saída esperada facilitando a vida do programador e futuras manutenções
- Redução de custos em manutenções.
- Fornece um bom design para a solução, pois uma aplicação testável deve ser bem organizada.
## TDD- TEST DRIVEN DEVELOPMENT
Desenvolvimento guiado por testes, é uma forma de desenvolver software, consiste primeiro em escrever o teste e depois implementar o método com as entradas e saídas esperadas.
### Vantagens
- Foco nos requisitos
- Tende a melhorar o design do código, deve ser testável.
- Menos chances de quebrar a aplicação
### Processo
1. Escrever teste
2. Implementar regra de negócio
3. Refatorar(conforme necessidade)
## Boas práticas e padrões
### Nomenclatura
-> <ação> should <EFEITO<> [when <Cenario<>] (opcional)
### Padrão AAA
+ **Arrange**: instanciar os objetos necessários
+ **Act**: executar as ações necessárias
+ **Assert**: declare o que deveria acontecer, resultado
### Independência/isolamento
+ Um teste não pode depender de outros testes, nem da ordem de execução.
### Único cenário
+ Deve ter uma lógica simples, linear
+ Testar apenas um caso(se um id existe, outro caso: se um id n existe)
+ Não usar condicionais ou loops
### Previsibilidade
+ O resultado de um teste deve ser sempre o mesmo para uma dada entrada de dados.
+ Não pode depender de fatores variáveis, como timestamp ou valores aleatórios.

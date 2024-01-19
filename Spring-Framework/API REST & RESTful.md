# Introdução
Uma API RESTful é uma aplicação na qual permite a comunicação entre um cliente/servidor enviando e recebendo dados por meio de protocolos HTTP com padrões de comunicação no  formato JSON/XML. 
Funciona como uma interface que permite a comunicação de diferentes tipos de aplicações, por exemplo mobile e desktop que consomem a mesma api para realizar suas funções.
Uma API pode ser considerada RESTful quando esta é implementada através da arquitetura REST, que consiste em um conjunto de boas práticas para construir e documentar a aplicação.
## Arquitetura REST
Modelo padrão para desenvolver aplicações de forma eficiente e gerando maior produtividade para os desenvolvedores. 
**Consiste de seis regras fundamentais:**
1. A aplicação deve separar suas responsabilidades, sendo cliente/servidor
2. Deve ser **stateless** não guardar o estado no servidor, cada resposta tem informações únicas e relevantes, não depende do servidor.
3.  Ser capaz de relizar cache, para reduzir o tráfego de dados entre cliente/servidor, aumentando a rapidez.
4. Interface uniforme, modelagem deve conter recursos bem definidos, utilizar os métodos HTTP e retornar os códigos adequados.
5. Construção em camadas, promovendo maior escalabilidade da aplicação em múltiplos servidores.
6. Capacidade de evoluir sem a quebra da aplicação, código sob demanda.
## Observações
Assuntos interessantes que devo me aprofundar:
 - [ ] Criando DTO utilizando java Records. 
+ [ ] **HATEOAS** : hipermídias que mostram o estado atual ou estados futuros e o relacionamento com os elementos por meio de links.
+ [ ] Padronização de datas, especialmente de forma global, utilizando @configuration e @bean no spring. [referencia](https://github.com/MichelliBrito/parking-control-api/blob/main/src/main/java/com/api/parkingcontrol/configs/DateConfig.java)

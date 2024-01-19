# Introdução
É uma arquitetura de software baseada na modularização dos serviços, que serão bem definidos e indepedentes entre si.
Exemplo:
![](img/microservices.png) 
## Vantagens
Esse tipo de arquitetura proporciona maior eficiência na manutenção e melhoria do produto, pois não há necessidade de parar todo o sistema, e sim apenas o módulo que será operado, dessa forma os demais serviços ainda poderão responder as requisições dos clientes.
Escalabilidade é um ponto forte, pois de forma flexível, podem ser aumentados apenas os módulos com maior necessidade (demanda). No monolítico seria necessário escalar toda a aplicação.
Cada microserviço pode ser construído na linguagem de programação que melhor atende.
Única vantagem de um sistema monolítico é na hora de fazer deploy, pois o microserviços requer maior complexidade por ter vários módulos.
## Comunicação entre MicroServiços
Para realizar a comunicação dos microserviços entre si, temos 2 formas de comunicação mais utilizadas: Protocolo HTTP através de api's REST e o protocolo AMQP que usa mensagerias.
O tipo de comunicação a ser utilizado leva em conta a necessidade da aplicação, se o sistema é síncrono ou assíncrono.
**Síncrono:** Utiliza-se do protocolo HTTP, através de apis que enviam e recebem dados para completar a o processo do serviço.
**Assíncrono:** Utiliza-se de mensageria, através do protocolo AMQP, entrega mensagens de um serviço ao outro, porém não  requer uma resposta, mas sim uma confirmação que a mensagem foi entregue.
## Spring e MicroServices
O Spring dispõe do módulo Spring Cloud, responsável por projetos prontos para implementar diversas funcionalidades
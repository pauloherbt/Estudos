# O que é JWT - Json Web Token 
É um padrão que define uma forma compacta e segura para transmitir informação entre diferentes dispositivos através de um objeto JSON.
É assinado digitalmente usando uma senha com o algoritmo **HMAC** ou uma chave pública/privada através de RSA ou ECDSA.
## Onde é utilizado ?
+ Autorização
Um token é gerado para um usuário logado, e cada requisição que ele fizer irá incluir o token, assim permitindo o usuário realizar a requisição, (rotas, serviços, e recursos).
## Estrutura de um token JWT
Basicamente consiste de três partes separadas por `.`
+ header
+ payload
+ signature
Exemplo:
`xxxxx.yyyyy.zzzzz`
### **Header**
O header contém o tipo do token, e especifica o algoritmo que está sendo usado para assinatura.
```json
{ 
	"alg": "HS256", 
	 "typ": "JWT" 
 }
```
Esse json está criptografado em Base64URL e forma a primeira parte do JWT.
### Payload
O payload é a segunda parte, nele contém os claims. 
**Claims** são declarações sobre uma entidade(normalmente o usuário) e alguns dados adicionais. Existem três tipos de claims: 
### Registered:
Um conjunto de claims predefinidas não obrigatórias, mas recomendadas, que proporcionam um conjunto de claims úteis e interoperáveis. Ex: **iss**(issuer), **exp** (expiration time), **sub**(subject) etc.
> Os nomes das claims costumam ser pequenos(3 letras) para manter o jwt compacto.
### Public:
Tem liberdade para serem definidas como quiserem, porém para evitar colisões, utilizase um padrão de nomeclatura definida no IANA JWT Registry.
### Private:
São os claims personalizados para compartilhar informações entre as partes e só são acessíveis por elas.

**Exemplo de payload**
```json
{ "sub": "1234567890", 
 "name": "John Doe", 
 "admin": true 
 }
```
**É codificado em base 64.**

> Percebe se que em tokens assinados, as informações no payload são visíveis por qualquer um. Não colocar informações sensíveis no payload ou header se o JWT não for encriptado!
## Signature
A assinatura é composta do header, o payload e uma senha, codificados e através de um algoritmo escolhido formam a assinatura. É utilizada para verificar se a mensagem foi alterada durante o caminho e pode verificar se quem envia o JWT é quem diz ser.
Ex utilizando o algoritmo HMAC SHA256
```json
HMACSHA256( 
base64UrlEncode(header) + "." + base64UrlEncode(payload), 
secret)
```
O resultado dessa assinatura é uma string codificada separada por pontos e compacta.
## Fluxo de uma aplicação
![](../img/Pasted%20image%2020240220155951.png)

![](../img/Pasted%20image%2020240220155839.png)

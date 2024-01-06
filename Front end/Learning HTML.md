## FreeCodeCamp project
Use apenas 1 h1 por pagina e os outros faz por ordem de importancia
- elemento “p” serve para criar paragrafos de texto;
- comentarios html <!— end with —>
- HTML5 possui elementos que delimitam diferentes areas de conteudo por ex:
- main /main nao esquecer identação]
- elemento <img src = “”> não precisa fechar, autofecha kk serve pra por imagem toda img precisa de um alt(propriedade do elemento)
- elemento anchor “a” serve pra redirecionar pra outra página syntax: a href = “” > precisa fechar
- Dentro de um paragrafo vc pode transformar qualquer texto em link com o anchor e href funciona com imagens tambem
- para fazer o link abrir uma nova aba use a propriedade target com o valor _blank
- elemento section para dividir em seções no exemplo apenas as fotos de gato
- link element para linkar um arquivo css pra estilizar
## Listas

### Lista não ordenada

não aparece a ordem dos itens

elemento ul
iniciar uma lista não ordenada (unordered list) 
dentro vc coloca os item lists (il) li> /li>

### Lista ordenada

mesma sintaxe da lista não ordenada mas ela exibe a numeração de cada item

list item il>

## Figure

permite voce adicionar uma imagem seguida de uma legenda para ela (no caso um elemento imagem)

figure> /figure>

figcaption> vc usa pra colcoar uma legenda ou descrição bem abaixo da foto

## Italico

vc pode usar o elemento em> para emfatizar

## Negrito

vc pode usar o elemento strong> pra deixar texto em negrito

## Formularios

Usado para recolher informações fornecidas pelo usuário e enviar para outro orgão.

- atributo **action** indica onde deve ser enviado os dados (path, url).

### Elementos de linha única:

- elemento **input** permite o usuario inserir algo, ele n precisa ser fechado
    - possui o atributo **type** para definir o que será a entrada.(radio, text)
    - atributo **id** para identificar um elemento da forma que eu quiser para facilitar a legibilidade do código
    - Atributo **placeholder** é aquela sombra que da uma dica do que tem que ter no campo.
    - Atributo **required** quando você impede o usuário de enviar o form sem nenhum dado (ele não precisa de valor, basta adicionar a palavra)
    - Atributo **********name********** facilita o processamento do formulario, especialmente qnd tem mts checkboxes, serve pra classificar o valor dos dados que serão passados no formulario, que são passados no par de atributos (**name/value**)

### Botões

- elemento **button** serve para executar uma ação, se não for especificada usará a ação do formulário.
- type radio **button →** pegar apenas uma opção entre várias.
- **checked** atributo → certificar de que pelo menos 1 botão ou checkbox serão selecionadas default

## Label

serve para delimitar conteudo dentro dele usado em conjunto com botoes, input type etc

## Fieldset

elemento usado para agrupar labels e inputs dentro de um elemento formulario

### Legend

É um atributo do fieldset, que serve para dar um contexto ao usuário sobre a input que ele deve colocar naquela parte do formulário.

## Footer Element

O rodapé da página é dado pelo elemento footer que é uma section
### Div Element
Usado para layout de design
## Estilizando elementos

Depois de ter compreendido o conceito de box-model, vamos aprender como manipular seus elementos através do CSS.

##### Padding e Margin

Atribuir um único valor ao padding ou margin diz ao css que esse valor será aplicado em todos os lados, mas também podemos atribuir valores diferentes para cada lado. 

- Valores para cada lado:
~~~css
    .post {
    ​	padding: 15px 10px 5px 0;
    }
~~~

Nesse caso, nós temos um valor para cada lado: 15px para o topo, 10px para a direita, 5px para a parte inferior e 0 para o lado esquerdo. Sempre será nessa ordem! 

- Valores utilizando propriedades específicas de cada lado:
~~~css
    .post {
        padding-top: 15px;
        padding-right: 10px;
        padding-bottom: 5px;
        padding-left: 0;
    }
~~~

Nesse caso estamos utilizando as propriedade específicas de cada lado. Essa abordagem é útil quando temos um padding ou margin com três lados iguais e um único diferente.



#### Propriedade Background

A propriedade background também é um atalho para várias outras propriedades. Podemos mudar a cor do fundo, colocar uma imagem no fundo e definir sua posição. Por enquanto, nesse curso introdutório vamos focar apenas no background-color. 

~~~css
    .post {
        background-color: green;
        background-color: #008800;
        background: #008800;
    }
~~~

Podemos indicar o valor de background-color de duas formas: nome da cor em inglês ou com o respectiva código hexadecimal.

Ainda podemos utilizar apenas a palavra "background" para definir a cor de fundo.



####  Border
A propriedade border pode assumir três valores: largura, cor e estilo.
~~~css
    .post {
        border: 3px solid blue;
        border-top: 2px dotted green;
        border-right: 4px dashed pink;
    }
~~~

Também podemos utilizar as propriedades específicas para cada aspecto da borda:
~~~css
    .post {
        border-width: 3px; <- Largura
        border-color: #505050; <- Cor
        border-style: solid; <- Estilo
    }
~~~

Ainda podemos criar uma regra mais específica juntando os aspectos com os lados da bordar:
~~~css
    .post {
        border-top-width: 3px;
        border-top-color: blue;
        border-top-style: solid;
    }
~~~

##### Border-radius

O border-radius permite arredondar os cantos de um elemento. A propriedade aceita várias unidades, mas as mais utilizadas é pixel e porcentagem. 

Colocando apenas um único valor, esse valor será aplicado em todos lados. Entretanto seguindo essa lógica de topo, direita, inferior e esquerda conseguimos alterar cada canto de forma separada.
~~~css
    .post {
        border-radius: 10px;
        border-radius: 50%;
        border-radius: 10% 20%;
        border-radius: 10% 20% 15% 22%
    }
~~~



## Estilizando textos

#### font-family

O font-family altera a fonte do nosso texto, nos permitindo utilizar fontes da web ou fontes instaladas na nossa máquina.
~~~css
    #title {
        font-family: Verdana;

    }

    .post_title {
        font-family: Verdana, Arial;
    }
~~~

#### font-size

O font-size altera o tamanho do nosso texto, sendo a unidade pixel mais utilizada.
~~~css
    #title {
        font-size: 30px;

    }

    .post_title {
        font-size: 18px;
    }
~~~

### fonte-style
O font-style altera a aparência do nosso texto. O valor padrão é 'normal' e vai nos exibir a fonte do jeito que foi desenhada. O valor 'italic' muda a fonte para itálico, mas temos que observar se a nossa fonte tem suporte ao itálico. Caso contrário, o navegador vai forçar a inclinação compromentendo a aparência do nosso projeto. 
~~~css
    #title {
        font-style: normal;

    }

    .subtitle {
        font-style: italic;
    }
~~~

### font-weight
O font-weight altera o "peso" do texto. Existem diversos tipos de valores para essa propriedade, mas são mais usado em fontes mais complexas que tem diversos pesos. As fontes mais simples limitam-se apenas ao valores 'normal' e 'bold'
~~~css
    #title {
        font-weight: normal;

    }

    .subtitle {
        font-weight: bold;
    }
~~~

### text-transform
O text-transforma altera a fonte entre maiusculas, minúsculas e capitalizada. 
O valor uppercase coloca todo o texto em caixa alta, o valor lowercase coloca o texto em caixa baixa e o valor capitalize coloca a primeira letra em caixa alta.
~~~css
    #title {
        text-transform: uppercase;

    }
    .subtitle {
        text-transform: lowercase;
    }
    .post_title {
        text-transform: capitalize;
    }
~~~

### text-decoration
O text-decoration é utilizado para dar destaque a algum texto. Essa propriedade nos permite colocar linhas sobre o texto.
O valor underline coloca uma linha abaixo do texto, o valor overline coloca uma linha acima e o valor line-through coloca uma linha ao centro, ou seja, cortando o texto.
~~~css
    #title {
        text-decoration: underline;

    }
    .subtitle {
        text-decoration: overline;
    }
    .post_title {
        text-decoration: line-through;
    }
~~~



## Estilizando listas

### list-style-type

O CSS nos permite alterar o marcador das listas (ordenadas ou não) através da propriedade list-style-type.

~~~css
    ul {
        list-style-type: square;
    }
    ol {
        list-style-type: upper-roman;
    }
    ul {
        list-style-type: "\1F44D";
    }
~~~

No exemplo acima, a primeira opção altera os marcadores de uma lista não ordenada para um quadrado. 
Na segunda opção, os marcadores de uma lista ordenada são trocados por números romanos. 
E na última opção, os marcadores de uma lista não ordenada são trocados por um emoji. Nesse caso, o emoji do joinha. 
Uma regra CSS é formada por um seletor ou grupo de seletores, que nada mais são do que elementos HTML. E dentro de um par de chaves definimos as declarações da regra de estilo. Uma declaração é formada por uma propriedade e um valor.

No exemplo abaixo estamos selecionando os elementos html (a, p, h1 e h3) e mudando sua cor para azul e o numero da font para 14 pixels.

    a, p, h1, h3 {
        color: blue;
        font-size: 14px;
    }

O seletor desse exemplo é um seletor de tipo. Isso significa que ele representa um elemento html e todo conteúdo contido nesse elemento sofrerá mudanças na aparência de acordo com as declarações. 

Para solucionar esses problemas temos os id e class que podem representar quaisquer tipo de elementos, seja de forma isolada ou em grupos. 

    <header id='header' class='header'></header>
    <header class="header"></header>


Há mais óbvia diferença entre class e id no HTML é sua forma de declaração usando saus respectivas palavras seguida de um nome. Já no CSS uma classe é precedida por um ponto e um id é precedido por um hash.

    .header{
        padding: 10px
    ​	}
    
    #header{
        padding: 15px;
    }


E a grande diferença entre id e class é que o mesmo id só pode ser usado uma vez na página, enquanto a classe serve pra agrupar elementos.  
# Introdução ao WebPaginismo: HTML
Nessa introdução veremos alguns conceitos básicos e como usar elementos de HTML para construir um site cru. Alguns exercícios parecem conter menos informação do que necessário, mas é importante que você sempre tente explorar vários caminhos (alguns deles darão errado) para chegar até a resposta e lembrar do que os exercícios anteriores te ensinarem. Continue testando possibilidades, mesmo depois de acertar um exercício. Quanto mais você trabalhar sua imaginação, mais rápido você vai entender a dinâmica do HTML.

## Como criar um arquivo HTML
1. Abra um editor de texto, como por exemplo o Bloco de Notas do Windows ou o [Atom](https://atom.io/);
2. Escreva o seu site;
3. Na hora de salvar, coloque a extensão `.html` no nome do arquivo:
    - `site.html`, por exemplo.
    - no Bloco de Notas do Windows, é necessário trocar de `*.txt` (arquivo de texto) para `*.*` (qualquer arquivo) nas opções de salvar.
4. Clique no seu arquivo com o botão direito, vá em 'Abrir com...' para decidir se você quer abrir com o navegador ou com o editor de texto.

## Tags
Nós definimos os elementos da nossa página (imagens, links, parágrafos, ...) usando _tags_. Uma tag é composta por seu nome e seus atributos. Elas são escritas em HTML dentro de símbolos de maior (`<`)  e menor (`>`). Por exemplo: `<elemento>`, onde `elemento` é o nome da tag.

#### Atributos
Seus atributos ficam dentro dos `<>`, após o nome e usando o símbolo `=` para atribuir um valor. Exemplo: `<elemento numero=0>`, onde `numero` é um atributo de `elemento` e seu valor é `0`.

#### Conteúdo
Algumas tags podem possuir algum tipo de conteúdo fora dos `<>`. Para mostrar que esse contéudo pertencem a elas, nós podemos "abrir" e "fechar" as tags para definir seus limites. Exemplo: `<elemento> conteudo </elemento>`. "conteudo" está dentro de `elemento` e usamos `/` no começo de uma tag para diferenciar uma tag de início de uma de fim.

## Hierarquia de Tags
Algumas tags podem possuir textos e outras tags dentro delas, dessa forma:
```html
<tag1>

    <tag2>

        <tag3>
            texto
        </tag3>

    </tag2>

    <tag4>

    </tag4>

</tag1>
```
Analisando, percebemos que:
- As tags `tag2` e `tag4` estão dentro da `tag1`, além de, por hieranquia, a `tag3` e o "texto";
- A `tag2` contém a `tag3` e, consequentemte, o "texto";
- A `tag3` só possui o "texto";
- A `tag4` está vazia.

Tags dentro de outras herdam características das suas tags-mãe.

## html, head e body
As tags mais importantes do HTML são:
- `<html>`: define o ínicio e fim de um documento HTML.
- `<head>`: contém informações sobre a página que o navegador usa para exibir corretamente e carregar recursos externos. As informações aqui não aparacem na página.
- `<body>`: delimita onde estão os elementos a serem exibidos na página, como textos e imagens.

## Exercícios
### Exercício 1
Coloque em um arquivo HTML as tags `<html>`, `<head>` e `<body>`. Dentro do `body` escreva uma frase que gostaria de dizer ao mundo. Os elementos que queremos que sejam exibidos na página ficam dentro de `body`.

_Dica: não esqueça de fechar as tags!_
``` html
<tag>
    ...
</tag>
```

### Exercício 2
Dê algum destaque a essa frase, usando alguma tag `<h1>`, `<h2>`, ... , `<h6>`.

### Exercício 3
Adicione um título para a sua página. Use a tag `<title>` dentro do `head`, escrevendo o título entre a abertura e fechamento da tag.

### Exercício 4
Mude a cor do plano de fundo do site.

_Dica: no_ `body` _tem um atributo para fazer isso, com a cor em código hexadecimal._
``` html
<body bgcolor=#9AFFF4>
```

### Exercício 5
Usando `<p>`, crie dois parágrafos. Com o atributo `align`, alinhe cada um de um jeito diferetente.

_Dica: alinhamentos suportados:_ `left`, `right`, `center` _e_ `justify`.

### Exercício 6
Escolha um site que você acha essencial o seu site ter um link. Use a tag `<a>` e o atributo `href` para levar um link para ter um link para esse site.

_Dica: o texto do link fica entre a tag_ `<a>`.
``` html
 <a href="website.net">Eu sou um link</a>
```

### Exercício 7
Toda boa página é recheada com as melhores imagens, não é mesmo? Escolha uma para colocar no seu site. A tag usada para isso é a `<img>` e o atributo com o endereço da imagem é `src`. `src` pode receber como valor o endereço de uma foto no seu computador (por exemplo, `src="foto.png"`, desde que `foto.png` esteja na mesma pasta que o seu `.html`)ou um link de uma imagem na internet. Você pode ajustar o tamanho da imagem com os atributos `width` e `height` (valores em pixel).


### Exercício 8
Alguns elementos estão mais próximos do que deveriam? Para adicionar mais linhas em branco, não adianta colocar linhas novas no seu `.html`. A tag `<br>` faz isso para você. Espalhe algumas pelo site para ver o resultado.

### Exercício 9
Para que nosso site possa exibir corretamente acentos, precisamos informar o navegador que o texto está na codificação [UTF-8](https://pt.wikipedia.org/wiki/UTF-8), que possui suporte para todas as letras do nosso alfabeto e mais uma infinidade de caracteres. Essa codificação é considerada o padrão da web pelo suporte a diferetentes idiomas e navegadores.
A linha em HTML que permite isso acontecer é a seguinte:
``` html
<meta charset="utf-8">
```
Onde essa linha deve ser inserida?

### Exercício 10
Coloque um link para qualquer página que, no lugar do texto, contenha uma imagem.
Coloque um outro link com algum `<hx>` no lugar do texto.

## Referências
[W3Schools.com](https://www.w3schools.com/tags/default.asp)

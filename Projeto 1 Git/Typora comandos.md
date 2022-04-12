# desafio-github-primeiro-repositório
# Markdown para Typora

## *Visão geral*

**Markdown** foi criado por [Daring Fireball](http://daringfireball.net/); a diretriz original é [aqui](http://daringfireball.net/projects/markdown/syntax). Sua sintaxe, no entanto, varia entre diferentes analisadores ou editores. **Typora** está usando [GitHub Flavored Markdown][GFM].

[toc]

## Elementos do bloco

### Quebras de parágrafo e linha

Um parágrafo é simplesmente uma ou mais linhas consecutivas de texto. No código-fonte markdown, os parágrafos são separados por duas ou mais linhas em branco. No Typora, você só precisa de uma linha em branco (pressione `Return` uma vez) para criar um novo parágrafo.

Pressione `Shift` + `Return` para criar uma única quebra de linha. A maioria dos outros analisadores de remarcação ignorarão quebras de linha simples, portanto, para fazer com que outros analisadores de remarcação reconheçam sua quebra de linha, você pode deixar dois espaços no final da linha ou inserir `<br/>`.

### Cabeçalhos

Os cabeçalhos usam 1-6 caracteres hash (`#`) no início da linha, correspondendo aos níveis de cabeçalho 1-6. Por exemplo:

``` remarcação
# Este é um H1

## Este é um H2

###### Este é um H6
```

Em Typora, insira ‘#’s seguido pelo conteúdo do título e pressione a tecla ‘Return’ para criar um cabeçalho.

### Citações em bloco

**Markdown** usa caracteres de estilo de e-mail > para citações em bloco. Eles são apresentados como:

``` remarcação
> Esta é uma citação em bloco com dois parágrafos. Este é o primeiro parágrafo.
>
> Este é o segundo pragraph. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.



> Esta é outra citação em bloco com um parágrafo. Há três linhas vazias para separar duas citações em bloco.
```

No Typora, inserir '>' seguido pelo conteúdo da cotação gerará um bloco de cotação. Typora irá inserir um '>' ou quebra de linha adequada para você. Citações de bloco aninhadas (uma citação de bloco dentro de outra citação de bloco) adicionando níveis adicionais de '>'.

### Listas

A entrada `* list item 1` criará uma lista não ordenada - o símbolo `*` pode ser substituído por `+` ou `-`.

Insira `1. list item 1` criará uma lista ordenada - seu código-fonte de remarcação é o seguinte:

``` remarcação
## lista não ordenada
*   Vermelho
*   Verde
*   Azul

## lista ordenada
1. Vermelho
2. Verde
3. Azul
```

### Lista de tarefas

Listas de tarefas são listas com itens marcados como [ ] ou [x] (incompletos ou completos). Por exemplo:

``` remarcação
- [ ] um item da lista de tarefas
- [ ] sintaxe de lista obrigatória
- [ ] normal **formatação**, @menções, #1234 referências
- [ ] incompleto
- [x] concluído
```

Você pode alterar o estado completo/incompleto clicando na caixa de seleção antes do item.

### Blocos de código (cercados)

Typora suporta apenas cercas no GitHub Flavored Markdown. Os blocos de código originais em markdown não são suportados.

Usar fences é fácil: Insira \`\`\` e pressione `return`. Adicione um identificador de idioma opcional após \`\`\` e vamos executá-lo através do realce de sintaxe:

```` gfm
Aqui está um exemplo:

``` js
teste de funcionamento() {
  console.log("observe a linha em branco antes desta função?");
}
```

realce de sintaxe:
``` rubi
exigir 'tapete vermelho'
markdown = Redcarpet.new("Olá Mundo!")
coloca markdown.to_html
```
````

### Blocos matemáticos

Você pode renderizar expressões matemáticas *LaTeX* usando **MathJax**.

Para adicionar uma expressão matemática, insira `$$` e pressione a tecla 'Return'. Isso acionará um campo de entrada que aceita a fonte *Tex/LaTex*. Por exemplo:


$$
\mathbf{V}_1 \times \mathbf{V}_2 = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} & \frac{\parcial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} & \frac{\parcial Y}{\partial v} & 0 \\
\end{vmatriz}
$$


No arquivo de origem do markdown, o bloco matemático é uma expressão *LaTeX* envolta por um par de marcas ‘$$’:

``` remarcação
$$
\mathbf{V}_1 \times \mathbf{V}_2 = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} & \frac{\parcial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} & \frac{\parcial Y}{\partial v} & 0 \\
\end{vmatriz}
$$
```

Você pode encontrar mais detalhes [aqui](https://support.typora.io/Math/).

### Tabelas

Insira `| Primeiro cabeçalho | Segundo Cabeçalho |` e pressione a tecla `return`. Isso criará uma tabela com duas colunas.

Depois que uma tabela é criada, colocar o foco nessa tabela abrirá uma barra de ferramentas para a tabela onde você pode redimensionar, alinhar ou excluir a tabela. Você também pode usar o menu de contexto para copiar e adicionar/excluir colunas/linhas individuais.

A sintaxe completa para tabelas está descrita abaixo, mas não é necessário conhecer a sintaxe completa em detalhes, pois o código-fonte de markdown para tabelas é gerado automaticamente pelo Typora.

No código-fonte markdown, eles se parecem com:

``` remarcação
| Primeiro cabeçalho | Segundo Cabeçalho |
| ------------- | ------------- |
| Célula de Conteúdo | Célula de Conteúdo |
| Célula de Conteúdo | Célula de Conteúdo |
```

Você também pode incluir Markdown embutido, como links, negrito, itálico ou tachado na tabela.

Por fim, incluindo dois pontos (`:`) na linha do cabeçalho, você pode definir o texto nessa coluna para ser alinhado à esquerda, à direita ou ao centro:

``` remarcação
| Alinhado à Esquerda | Alinhado ao Centro | Alinhado à direita |
| :------------ |:---------------:|
```

-----:|
| col 3 é | algum texto prolixo | $ 1600 |
| col 2 é | centrado | $ 12 |
| listras de zebra | são puros | $1 |
```

Dois pontos no lado esquerdo indica uma coluna alinhada à esquerda; dois pontos no lado mais à direita indica uma coluna alinhada à direita; dois pontos em ambos os lados indicam uma coluna alinhada ao centro.

### Notas de rodapé

``` remarcação
Você pode criar notas de rodapé como esta[^footnote].

[^nota de rodapé]: Aqui está o *texto* da **nota de rodapé**.
```

vai produzir:

Você pode criar notas de rodapé como esta[^footnote].

[^nota de rodapé]: Aqui está o *texto* da **nota de rodapé**.

Passe o mouse sobre o sobrescrito 'nota de rodapé' para ver o conteúdo da nota de rodapé.

### Regras horizontais

Inserir `***` ou `---` em uma linha em branco e pressionar `return` desenhará uma linha horizontal.

------

### Assunto principal do YAML

Typora agora suporta [YAML Front Matter](http://jekyllrb.com/docs/frontmatter/). Insira `---` na parte superior do artigo e pressione `Return` para introduzir um bloco de metadados. Alternativamente, você pode inserir um bloco de metadados no menu superior do Typora.

### Índice (TOC)

Insira `[toc]` e pressione a tecla `Return`. Isso criará uma seção "Índice". O sumário extrai todos os cabeçalhos do documento e seu conteúdo é atualizado automaticamente à medida que você adiciona ao documento.

## Elementos de extensão

Os elementos Span serão analisados e renderizados logo após a digitação. Mover o cursor no meio desses elementos de extensão expandirá esses elementos na origem de remarcação. Abaixo está uma explicação da sintaxe para cada elemento span.

### Links

O Markdown suporta dois estilos de links: inline e de referência.

Em ambos os estilos, o texto do link é delimitado por [colchetes].

Para criar um link embutido, use um conjunto de parênteses regulares imediatamente após o colchete de fechamento do texto do link. Dentro dos parênteses, coloque a URL para onde você quer que o link aponte, junto com um título opcional para o link, entre aspas. Por exemplo:

``` remarcação
Este é um link embutido [um exemplo](http://example.com/ "Título").

[Este link](http://example.net/) não tem atributo de título.
```

vai produzir:

Este é um link embutido [um exemplo](http://example.com/ "Título"). (`<p>Este é <a href="http://example.com/" title="Title">`)

[Este link](http://example.net/) não tem atributo de título. (`<p><a href="http://example.net/">Este link</a> não tem`)

#### Links internos

**Você pode definir o href para cabeçalhos**, o que criará um marcador que permitirá que você vá para essa seção depois de clicar. Por exemplo:

Comando(no Windows: Ctrl) + Clique em [Este link](#block-elements) irá pular para o cabeçalho `Block Elements`. Para ver como escrever isso, mova o cursor ou clique nesse link com a tecla `⌘` pressionada para expandir o elemento na fonte de remarcação.

#### Links de referência

Links de estilo de referência usam um segundo conjunto de colchetes, dentro do qual você coloca um rótulo de sua escolha para identificar o link:

``` remarcação
Este é [um exemplo][id] link de estilo de referência.

Então, em qualquer lugar do documento, você define seu rótulo de link em uma linha assim:

[id]: http://example.com/ "Título opcional aqui"
```

Em Typora, eles serão renderizados assim:

Este é [um exemplo][id] link de estilo de referência.

[id]: http://example.com/ "Título opcional aqui"

O atalho do nome do link implícito permite que você omita o nome do link, caso em que o próprio texto do link é usado como nome. Basta usar um conjunto vazio de colchetes – por exemplo, para vincular a palavra “Google” ao site google.com, você pode simplesmente escrever:

``` remarcação
[Google][]
E então defina o link:

[Google]: http://google.com/
```

No Typora, clicar no link o expandirá para edição e command+click abrirá o hiperlink em seu navegador da web.

### URLs

Typora permite que você insira URLs como links, envoltos por `<`colchetes`>`.

`<i@typora.io>` torna-se <i@typora.io>.

Typora também vinculará automaticamente URLs padrão. por exemplo: www.google.com.

### Imagens

As imagens têm sintaxe semelhante aos links, mas requerem um caractere `!` adicional antes do início do link. A sintaxe para inserir uma imagem é assim:

``` remarcação
![Texto alternativo](/path/to/img.jpg)

![Texto alternativo](/path/to/img.jpg "Título opcional")
```

Você pode usar arrastar e soltar para inserir uma imagem de um arquivo de imagem ou do seu navegador da web. Você pode modificar o código-fonte do markdown clicando na imagem. Um caminho relativo será usado se a imagem adicionada usando arrastar e soltar estiver no mesmo diretório ou subdiretório do documento que você está editando no momento.

Se você estiver usando markdown para criar sites, poderá especificar um prefixo de URL para a visualização da imagem em seu computador local com a propriedade `typora-root-url` em YAML Front Matters. Por exemplo, insira `typora-root-url:/User/Abner/Website/typora.io/` no YAML Front Matters e, em seguida, `![alt](/blog/img/test.png)` será tratado como `![alt](file:///User/Abner/Website/typora.io/blog/img/test.png)` em Typora.

Você pode encontrar mais detalhes [aqui](https://support.typora.io/Images/).

### Ênfase

Markdown trata asteriscos (`*`) e sublinhados (`_`) a

s indicadores de ênfase. O texto agrupado com um `*` ou `_` será agrupado com uma tag HTML `<em>`. Por exemplo:

``` remarcação
*asteriscos simples*

_sublinhados simples_
```

saída:

*asteriscos simples*

_sublinhados simples_

O GFM ignorará sublinhados em palavras, o que é comumente usado em códigos e nomes, como este:

> wow_great_stuff
>
> faça_isso_e_faça_isso_e_outra_coisa.

Para produzir um asterisco ou sublinhado literal em uma posição onde de outra forma seria usado como delimitador de ênfase, você pode escapar da barra invertida:

``` remarcação
\*este texto está cercado por asteriscos literais\*
```

Typora recomenda usar o símbolo `*`.

### Forte

Um duplo `*` ou `_` fará com que seu conteúdo seja encapsulado com uma tag HTML `<strong>`, por exemplo:

``` remarcação
**Asteriscos duplos**

__sublinhados duplos__
```

saída:

**Asteriscos duplos**

__sublinhados duplos__

Typora recomenda usar o símbolo `**`.

### Código

Para indicar um intervalo de código embutido, envolva-o com aspas (`). Ao contrário de um bloco de código pré-formatado, uma extensão de código indica o código dentro de um parágrafo normal. Por exemplo:

``` remarcação
Use a função `printf()`.
```

vai produzir:

Use a função `printf()`.

### Tachado

O GFM adiciona sintaxe para criar texto tachado, que está faltando no Markdown padrão.

`~~Texto errado.~~` torna-se ~~Texto errado.~~

### Sublinhadas

O sublinhado é alimentado por HTML bruto.

`<u>Sublinhado</u>` torna-se <u>Sublinhado</u>.

### Emoji :smile:

Insira o emoji com a sintaxe `:smile:`.

O usuário pode acionar sugestões de preenchimento automático para emoji pressionando a tecla 'ESC' ou acioná-lo automaticamente após habilitá-lo no painel de preferências. Além disso, a entrada direta de caracteres emoji UTF-8 também é suportada acessando `Edit` -> `Emoji & Symbols` na barra de menus (macOS).

### Matemática Inline

Para usar este recurso, habilite-o primeiro no Painel `Preference` -> Aba `Markdown`. Em seguida, use `$` para envolver um comando TeX. Por exemplo: `$\lim_{x \to \infty} \exp(-x) = 0$` será renderizado como comando LaTeX.

Para acionar a visualização inline para matemática inline: insira “$”, pressione a tecla 'ESC' e insira um comando TeX.

Você pode encontrar mais detalhes [aqui](https://support.typora.io/Math/).

### Subscrito

Para usar este recurso, habilite-o primeiro no Painel `Preference` -> Aba `Markdown`. Em seguida, use `~` para envolver o conteúdo do subscrito. Por exemplo: `H~2~O`, `X~long\text~`/

### Sobrescrito

Para usar este recurso, habilite-o primeiro no Painel `Preference` -> Aba `Markdown`. Em seguida, use `^` para envolver o conteúdo sobrescrito. Por exemplo: `X^2^`.

### Destaque

Para usar este recurso, habilite-o primeiro no Painel `Preference` -> Aba `Markdown`. Em seguida, use `==` para envolver o conteúdo de destaque. Por exemplo: `==destaque==`.

## HTML

Você pode usar HTML para estilizar o conteúdo que o Markdown puro não suporta. Por exemplo, use `<span style="color:red">este texto é vermelho</span>` para adicionar texto com a cor vermelha.

### Incorporar conteúdo

Alguns sites fornecem código de incorporação baseado em iframe que você também pode colar no Typora. Por exemplo:

```Remarcação
<iframe height='265' scrolling='no' title='Menu SVG animado sofisticado' src='http://codepen.io/jeangontijo/embed/OxVywj/?height=265&theme-id=0&default-tab=css, result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>
```

### Vídeo

Você pode usar a tag HTML `<video>` para incorporar vídeos. Por exemplo:

```Remarcação
<video src="xxx.mp4" />
```

### Outros suportes HTML

Você pode encontrar mais detalhes [aqui](https://support.typora.io/HTML/).

[GFM]: https://help.github.com/articles/github-flavored-markdown/











## Links Úteis

[https://github.com/alex231181/desafio-github-primeiro-repositori.git]

[https://typora.io/]

[https://web.dio.me/]

[https://translate.google.com/]


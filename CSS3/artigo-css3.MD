Universidade do Oeste de Santa Catarina<br/>
Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob<br/>
Disciplina: Desenvolvimento com HTML5 e CSS3<br/>
Professor: Jean Carlo Nascimento<br/>
Acadêmico: Ednilson Fernando Devilla<br/>

#**CSS3**

###**1.	Funcionalidade: Negação**
<br/>
**O que é?**<br/>
É a negação de um elemento
<br/>
**Onde usar:**<br/>
Em qualquer elemento que possa ser negado

Quando todos os parágrafos já tem um estilo de cor definido e precisa destacar uma cor
diferente em um outro paragrafo do texto, usando uma classe resolve. Abaixo segue o exemplo.

Uma forma de se fazer é com elementos que não batem naquela regra, isso quer dizer que, queremos todos os parágrafos que não têm a classe especial. A sintaxe do *:not()* recebe como argumento algum outro seletor simples como classes, id ou tags. Abaixo o exemplo.<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo CSS :not()<br>

	`<p>Texto de exemplo</p>`<br/>
	`<p>Texto de exemplo</p>`<br/> 
	`<p class="especial">Texto de exemplo especial</p>`<br/>
	`<p>Mais textos de exemplos</p>`<br/>
	**CSS**<br/>
`p:not(.especial){`<br/>
  `color: gray;`<br/>
`}`

* Referencia: http://www.maujor.com/tutorial/sel-css3.php/.<br/>

###2.	Funcionalidade: Pseudo-classes <br/>
**O que é?**<br/>
Quando se quer mudar a cor do primeiro e do ultimo elemento de uma lista, com elementos que já são pré definidos os elementos são chamamos de pseudo-classes. O primeiro elemento chamamos de *first-child* e o ultimo elemento de *last-child*. O HTML fica igual. <br/>

**Onde usar:**<br/>
Geralmente utlizados em listas<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo HTML<br/>
`<ul>`<br/>
  `<li>Primeiro item</li>`<br/>
  `<li>Segundo item</li>`<br/>
  `<li>Terceiro item</li>`<br/>
  `<li>Quarto item</li>`<br/>
`</ul>`

No CSS, podemos usar pseudo-classes, repare no exemplo apresentado no quadro 5 é que mudou o operador de ponto para dois pontos, diferenciando um do outro.<br/>

Exemplo CSS<br/>
`li:first-child{`<br/>
  `color: red;`<br/>
`}`<br/>
`li:last-child{`<br/>
  `color: blue;`<br/>
`}`
<br/>
O exemplo acima mostra o uso de pseudo-classes em listas<br/>

* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/

###3. Funcionalidade: Pseudo elementos<br/>
**O que é?**<br/>
Pseudo elementos são elementos que não existem no documento HTML mas podem ser selecionados através do CSS. Por exemplo o HTML fica de uma forma normal.<br/>

**Onde usar:**<br/>
Em elementos que tenham mais de um elemento<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo HTML<br>
`<p>Exemplo de texto no HTML!</p>`
<br/>
Modifica apenas a primeira letra.<br/>
Exemplo CSS<br>
`p:first-letter{`
  `font-size: 200%;`
`}`

Existe também outro Pseudo elemento que seleciona apenas a primeira linha.<br/>
Exemplo CSS<br/>
`p:first-line{`<br/>
  `font-style: italic;`<br/>
`}`
* Referencia: http://www.w3c.br/pub/Cursos/CursoCSS3/css-web.pdf
<br/>

###4.Funcionalidade: Transitions<br/>
**O que é e onde usar?**<br/>
Com as transitions conseguimos animar o processo de mudança de algum valor do CSS. Por exemplo, temos um elemento na posição *top:20px* e, quando passarmos o mouse em cima (*hover*), queremos que o elemento vá para *top:40px*.<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo CSS<br/>
`#teste{`<br/>
  `position: relative;`<br/>
  `top: 0;`<br/>
`}`<br/>
`#teste:hover{`<br/>
  `top: 30px;`<br/>
`}`
<br/>

No exemplo acima o elemento é deslocado de uma vez, quando passamos o mouse em cima, caso queira que o elemento mude suavemente basta usar o código apresentado exemplo abaixo.<br/>

Exemplo CSS<br/>
`#teste:hover{`<br/>
  `transition: top 2s;`<br/>
`}`
<br/>
Isso indica que queremos animar a propriedade top durante 2 segundos.

Por padrão, a animação é linear, mas temos outros tipos para animações mais suaves:
<br/>
Exemplo de animações<br/>
**linear** - `velocidade constante na animação;`<br/>
**ease** - `redução gradual na velocidade da animação;`<br/>
**ease-in** - `aumento gradual na velocidade da animação;`<br/>
**ease-in-out** - `aumento gradual, depois redução gradual na velocidade da animação;`<br/>
**cubic-bezier**`(x1,y1,x2,y2) - curva de velocidade para animação customizada (avançado);`

<br/>
Exemplo CSS<br/>
`#teste:hover{`<br/>
  `transition: top 2s ease;`<br/>
`}`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/ 

###5.Funcionalidade: Transforms<br/>

**O que é?**<br/>
Através dessa nova especificação é possível alterar propriedades visuais dos elementos. Por exemplo, mostre uma escala maior ou menor que seu tamanho padrão ou alterar a posição do elemento sem sofrer interferência de sua estrutura.<br/>

No exemplo apresenta-se a propriedade *transalate*.<br/>

####5.1 Translate<br/>
**O que é?**<br/>
Move os elementos entre os eixos X e Y.<br/>
**Onde usar?**<br/>
Em elementos que estejam entre os eixos X e Y<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo CSS<br/>
`.header{`<br/>
  `/* Move o elemento no eixo horizontal */`<br/>
  `transform: translateX(50px);`<br/>
`}`<br/>
`#main{`<br/>
  `/* Move o elemento no eixo vertical */`<br/>
  `transform: translateY(-20px);`<br/>
`}`<br/>
`footer{`<br/>
  `/* Move o elemento nos dois eixos (X, Y) */`<br/>
  `transform: translate(40px, -20px);`<br/>
`}`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/>

####5.2 Rotate<br/>
**O que é?**<br/>
Rotacão de elementos.<br/>
**Onde usar?**<br/>
Em elementos que possam ser rotacionados<br/>
**Como usar e exemplo de uso:**<br/>
Exemplo de CSS, que rotaciona os elementos.<br/>
`#menu-departamentos{`<br/>
  `transform: rotate(-10deg);`<br/>
`}`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/>

####5.3 Scale<br/>
**O que é?**<br/>
Altera escalas de elementos.<br/>
**Onde usar?**<br/>
Em elementos que possam ser alterados as escalas<br/>
**Como usar e exemplo de uso:**<br/>
Exemplo de CSS, scale.<br/>

`#novidades li{`<br/>
  `/* Alterar a escala total do elemento */`<br/>
  `transform: scale(1.2);`<br/>
`}`<br/>
`#mais-vendidos li{`<br/>
  `/* Alterar a escala vertical e horizontal do elemento */`<br/>
  `transform: scale(1, 0.6);`<br/>
`}`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/>

####5.4 Skew<br/>
**O que é?**<br/>
Distoção de elementos
**Onde usar?**<br/>
Em elementos que possam sofrer distorção<br/>
**Como usar e exemplo de uso:**<br/>

Exemplo CSS, distorce os elementos selecionados.<br/>

`footer{`<br/>
  `/* Distorcer o elemento no eixo horizontal */`<br/>
  `transform: skewX(10deg);`<br/>
`}`<br/>
`#social{`<br/>
  `/* Distorcer o elemento no eixo vertical */`<br/>
  `transform: skewY(10deg);`<br/>
`}`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/>

###6.Funcionalidade: Seletores avançados<br/>

####6.1 Seletor de irmãos<br/>
**O que é?**<br/>
O seletor de irmãos (~) indica que queremos selecionar todos os `<p>` que foram precedidos por algum `<h2>` e são irmãos do subtítulo (ou seja, estão sob a mesma tag pai). <br/>

**Onde usar?**<br/>
Em elementos que tenham varias tags que estão sob uma tag pai<br/>

**Como usar e exemplo de uso:**<br/>
No exemplo apresenta-se um HTML que simula vários parágrafos, títulos e subtítulos em um documento.<br/>

Exemplo HTML<br/>
`<article>`<br/>
  `<h1>Título</h1>`<br/>
  `<p>Início</p>`<br/>
  `<h2>Subtítulo</h2>`<br/>
  `<p>Texto</p>`<br/>
  `<p>Mais texto</p>`<br/>
`</article>`<br/>

Exemplo CSS, seletor de irmãos<br/>
`h2 ~ p{`<br/>
  `font-style: italic;`<br/>
`}`
<br/>
* Referencia: http://maujor.com/tutorial/seletores_css21_parte2.php<br/>

####6.2 Seletor de irmão adjacentes<br/>
**O que é?**<br/>
Utilizando o HTML apresentado no exemplo acima, quando se quer selecionar o paragrafo `<p>` e seguinte já existe um subtítulo `<h2>`, utilizamos o seletor de irmãos adjacentes.<br/>
**Onde usar?**<br/>
Em elementos devem ter o mesmo pai e o primeiro elemento deve ser imediatamente anterior ao segundo.<br/>
**Como usar e exemplo de uso:**<br/>
Exemplo CSS com seletor de irmão adjacentes<br/>
`h2 + p{`<br/>
  `font-variant: small-caps;`<br/>
`}`
<br/>
Nesse caso apenas o texto será selecionado.<br/>
* Referencia: http://maujor.com/tutorial/seletores_css21_parte2.php<br/>

###7. Funcionalidade: Text-shadow<br/>
**O que é?**<br/>
O text-shadow serve para colocar sombras em textos. <br/>
**Onde usar?**<br/>
Em textos
**Como usar e exemplo de uso:**<br/>
Sua sintaxe é fácil de entender, recebe-se o deslocamento da sombra e a cor.<br/>
Exemplo CSS, text-shadow<br/>
`p{`<br/>
  `text-shadow: 10px 10px red;`<br/>
`}`<br/>

É possível até passar mais de uma sombra ao mesmo tempo para o mesmo elemento:<br/>
Exemplo CSS, passando mais de uma sombra<br/>

`text-shadow: 10px 10px 5px red, -5px -5px 4px red;`
* Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/> 

###8. Funcionalidade: Box-shadow<br/>
**O que é e onde usar?**<br/>
Podemos colocar sombras em qualquer elemento com o box-shadow.<br/>

**Como usar e exemplo de uso:**<br/>
A sintaxe é parecida com a do text-shadow, deslocamento da sombra e a cor.<br/>

Exemplo CSS com box-shadow<br/>
`box-shadow: 20px 20px black;`
<br/>

O box-shadow suporta mais um valor que faz a sombra aumentar ou diminuir, vejamos o exemplo no quadro 24<br/>
Exemplo CSS<br/>
`box-shadow: 20px 20px 20px 30px black;`
* Fonte: Referencia: http://www.caelum.com.br/apostila-html-css-javascript/css-avancado/<br/>

###9. Funcionalidade: Opacidade e RGBA<br/>
**O que é e onde usar?**<br/>
É possível mudar a opacidade de um elemento para que ele seja mais transparente com o uso da propriedade *opacity*. É simples, a propriedade *opacity* recebe um valor decimal entre 0 e 1, vejamos o exemplo.<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo CSS, opacity<br/>

`p{`<br/>
  `opacity: 0.3;`<br/>
`}`<br/>

Além das cores hexadecimais normais (#FFFFFF pro branco), podemos criar cores a partir de seu valor RGB, passando o valor de cada canal (Red, Green, Blue) separadamente (valor entre 0 e 255).<br/>
Exemplo CSS, com todas equivalentes<br/>
`color: #FFFFFF;`<br/>
`color: white;`<br/>
`color: rgb(255, 255, 255);`
<br/>

Porém, existe uma função chamada RGBA que recebe um quarto argumento, o chamado canal Alpha. Na prática, seria como o *opacity* daquela cor (um valor entre 0 e 1), vejamos no quadro 27.<br/>
Quadro 27: Exemplo CSS, com a função RGBA<br/>
`/* branco com 80% de opacidade */`<br/>
`color: rgba(255,255,255, 0.8);`
* Referencia: http://www.w3c.br/pub/Cursos/CursoCSS3/css-web.pdf<br/>
 
###10. Funcionalidade: Gradientes<br/>
**O que é e onde usar?**<br/>
O CSS3 traz suporte a declaração de gradientes sem que se precise trabalhar com imagens, além de ser simples a página fica mais leve e a renderização fica melhor por se adaptar a todos os tipos de resolução. Existe suporte a gradientes lineares e radiais. No exemplo abaixo podemos ver melhor a sintaxe básica.<br/>

**Como usar e exemplo de uso:**<br/>
Exemplo CSS de gradiente<br/>
`.linear{`
  `background: linear-gradient(white, blue);`<br/>
`}`<br/>
`.radial{`<br/>
  `background: radial-gradient(white, blue);`<br/>
`}`<br/>
 
No exemplo acima apresenta-se os exemplos dos tipos de gradientes lineares e radias, passando as cores branco (*white*) e azul (*blue*).<br/>
	Podemos ainda usar gradientes com angulações diferentes e diversas paradas de cores.<br/>
Exemplo CSS com angulações diferentes<br/>
`.gradiente {`<br/>
  `background: linear-gradient(45deg, #f0f9ff 0%, #cbebff 47%, #a1dbff 100%);`<br/>
`}`
* Referencia: http://www.w3c.br/pub/Cursos/CursoCSS3/css-web.pdf<br/>
 
###11. Funcionalidade: Foco<br/>
**O que é e onde usar?**<br/>
Coloca o foco no elemento quando ele for selecionado, no exemplo no quadro 30 apresenta o HTML normal, a única mudança ocorre no CSS.<br/>
**Como usar e exemplo de uso:**<br/>
Exemplo HTML<br/>
`<input type="text">`<br/>
Veja que o HTML não muda, acima apresenta um simples input do tipo text, no quadro 31 apresenta o CSS referente ao quadro 30.<br/>
 
 Exemplo CSS, quando o foco está no input<br/>
`input:focus{`<br/>
    `background: yellow;`<br/>
    `border: 1px solid black;`<br/>
`}`<br/>
No exemplo acima apresenta que quando o foco está no input, à cor dele muda para amarelo (*yellow*), quando o foco sai do input a cor volta ao normal.
* Referencia: http://www.w3c.br/pub/Cursos/CursoCSS3/css-web.pdf<br/>
 
###12.Funcionalidade: Prefixos<br/>
**O que é e onde usar?**<br/>
Muitos dos novos recursos do CSS3 ainda são experimentais , isso quer dizer que foram incluídos nos rascunhos, mas ainda não são 100% oficias. As especificações ainda estão em aberto e vai demorar um pouco até serem finalizadas.<br/>
	Existem recursos mais estáveis e menos estáveis. Por outro lado, alguns são bem recentes e talvez ainda possa haver mudança até a aprovação final da especificação.<br/>
	Os navegadores desejam implementar os novos recursos antes mesmo da especificação terminar, para que os desenvolvedores possam começar a usar as novas propriedades e experimentá-las na prática. Entretanto, como a sintaxe final depois de aprovada pode ser diferente, os navegadores implementam as novas propriedades instáveis usando nomes provisórios.<br/>
	Uma boa pratica na utilização é pegar o nome da propriedade e colocar um prefixo na especifico do fabricante na frente. Quando a especificação ficar estável tira-se o prefixo e deixa-se a sintaxe oficial.<br/>
Os prefixos dos fabricantes mais usados são:<br/><br/>
Prefixos dos fabricantes mais usados<br/>
**-webkit-**`: navegadores Webkit (Chrome, Safari, iOS, Android)`<br/>
**-moz-**`: Firefox (Mozilla)`<br/>
**-ms-**`: Internet Explorer (Microsoft)`<br/>
**-o-**`: Opera`<br/>
**Como usar e exemplo de uso:**<br/>
Utilizando os prefixos no CSS<br/>
`p{`<br/>
  `/* Chrome até versão 3, Safari até versão 4 */`<br/>
  `-webkit-border-radius: 5px;`<br/>
  `/* Firefox até 3.6 */`<br/>
  `-moz-border-radius: 5px;`<br/>
  `/* Todas as versões modernas dos navegadores, `<br/>
   `incluindo IE e Opera que nunca precisaram de `<br/>
   `prefixo pra isso */`<br/>
  `border-radius: 5px;`<br/>
`}`<br/>
	No exemplo acima apresenta-se a utilização de prefixos utilizados no border-radius, fazendo com que o border-radius funcione em diversos navegadores, sem que sofra qualquer alteração.<br/>

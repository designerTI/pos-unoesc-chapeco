Universidade do Oeste de Santa Catarina<br/>
Disciplina: Desenvolvimento com HTML5 e CSS3<br/>
Professor: Jean Carlo Nascimento<br/>
Acadêmico: Ednilson Fernando Devilla<br/>

#**CSS3**

###**1.	Negação**

Quando todos os parágrafos já tem um estilo de cor definido e precisa destacar uma cor
diferente em um outro paragrafo do texto, usando uma classe resolve. Abaixo segue o exemplo.

####HTML
Quadro 1: Exemplo HTML.<br/>
	`<p>Texto de exemplo</p>`<br/>
	`<p>Texto de exemplo</p>`<br/> 
	`<p class="especial">Texto de exemplo especial</p>`<br/>
	`<p>Mais textos de exemplos</p>`
	
* Fonte: W3C, (2014).<br/><br/>

####CSS<br/>
Quadro 2: Exemplo CSS<br/>
`p{`<br/>
  `color: gray;`<br/>
`}`<br/>
`p.especial{`<br/>
  `color: black; /* cor do texto especial */`<br/>
`}`
* Fonte: W3C, (2014).<br/>

Outra forma de se fazer é com elementos que não batem naquela regra, isso quer dizer que, queremos todos os parágrafos que não têm a classe especial. A sintaxe do *:not()* recebe como argumento algum outro seletor simples como classes, id ou tags. Abaixo o exemplo.<br/>

####CSS<br/>
Quadro 3: Exemplo CSS :not()<br>
`p:not(.especial){`<br/>
  `color: gray;`<br/>
`}`

* Fonte: W3C, (2014).<br/>

###2.	Pseudo-classes <br/>
Quando se quer mudar a cor do primeiro e do ultimo elemento de uma lista, com elementos que já são pré definidos os elementos são chamamos de pseudo-classes. O primeiro elemento chamamos de *first-child* e o ultimo elemento de *last-child*. O HTML fica igual, vejamos o exemplo no quadro abaixo. <br/>

Quadro 4: Exemplo HTML<br/>
`<ul>`<br/>
  `<li>Primeiro item</li>`<br/>
  `<li>Segundo item</li>`<br/>
  `<li>Terceiro item</li>`<br/>
  `<li>Quarto item</li>`<br/>
`</ul>`
* Fonte: Caelum, (2010).<br/> 

No CSS, podemos usar pseudo-classes, repare no exemplo apresentado no quadro 5 é que mudou o operador de ponto para dois pontos, diferenciando um do outro.<br/>

Quadro 5: Exemplo CSS<br/>
`li:first-child{`<br/>
  `color: red;`<br/>
`}`<br/>
`li:last-child{`<br/>
  `color: blue;`<br/>
`}`
* Fonte: Caelum, (2010).
<br/>

### **3. Pseudo elementos**<br/>
Pseudo elementos são elementos que não existem no documento HTML mas podem ser selecionados através do CSS. Por exemplo o HTML fica de uma forma normal como apresentado no quadro 6.<br/>

Quadro 6: Exemplo HTML<br>
`<p>Exemplo de texto no HTML!</p>`
* Fonte: Maujor, (2006).<br/>
 
O CSS apresentado no quadro 7, modifica apenas a primeira letra.<br/>
Quadro 7: Exemplo CSS<br>
`p:first-letter{`
  `font-size: 200%;`
`}`
* Fonte: Maujor, (2006).<br/>
 
Existe também outro Pseudo elemento que seleciona apenas a primeira linha.<br/>
Quadro 8: Exemplo CSS<br/>
`p:first-line{`<br/>
  `font-style: italic;`<br/>
`}`
* Fonte: Maujor, (2006).<br/>
 
###4.	Transitions<br/>

Com as transitions conseguimos animar o processo de mudança de algum valor do CSS. Por exemplo, temos um elemento na posição *top:20px* e, quando passarmos o mouse em cima (*hover*), queremos que o elemento vá para *top:40px*. No quadro 9 podemos ver o exemplo.<br/>
Quadro 9: Exemplo CSS<br/>
`#teste{`<br/>
  `position: relative;`<br/>
  `top: 0;`<br/>
`}`<br/>
`#teste:hover{`<br/>
  `top: 30px;`<br/>
`}`
* Fonte: Caelum, (2010)
<br/>

No exemplo acima o elemento é deslocado de uma vez, quando passamos o mouse em cima, caso queira que o elemento mude suavemente basta usar o código apresentado no quadro 10.<br/>

Quadro 10: Exemplo CSS<br/>
`#teste:hover{`<br/>
  `transition: top 2s;`<br/>
`}``
* Fonte: Caelum, (2010)
<br/>
Isso indica que queremos animar a propriedade top durante 2 segundos.

Por padrão, a animação é linear, mas temos outros tipos para animações mais suaves:
<br/>
Quadro 11: Exemplo de animações<br/>
**linear** - `velocidade constante na animação;`<br/>
**ease** - `redução gradual na velocidade da animação;`<br/>
**ease-in** - `aumento gradual na velocidade da animação;`<br/>
**ease-in-out** - `aumento gradual, depois redução gradual na velocidade da animação;`<br/>
**cubic-bezier**`(x1,y1,x2,y2) - curva de velocidade para animação customizada (avançado);`
* Fonte: Caelum, (2010).
<br/>
Quadro 12: Exemplo CSS<br/>
`#teste:hover{`<br/>
  `transition: top 2s ease;`<br/>
`}`
* Fonte: Caelum, (2010)<br/>

###5.	Transforms<br/>

Através dessa nova especificação é possível alterar propriedades visuais dos elementos. Por exemplo, mostre uma escala maior ou menor que seu tamanho padrão ou alterar a posição do elemento sem sofrer interferência de sua estrutura.<br/>

No quadro 13 apresenta-se a propriedade *transalate*.<br/>

####5.1 Translate<br/>
Move os elementos entre os eixos X e Y.<br/>

Quadro 13: Exemplo CSS<br/>
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
* Fonte: W3C, (2014).<br/>

####5.2 Rotate<br/>
Rotaciona os elementos.<br/>

Quadro 14: Exemplo de CSS, que rotaciona os elementos.<br/>
`#menu-departamentos{`<br/>
  `transform: rotate(-10deg);`<br/>
`}`
* Fonte: W3C, (2014).<br/>

####5.3 Scale<br/>

Altera escalas de elementos.<br/>
Quadro 15: Exemplo de CSS, scale.<br/>

`#novidades li{`<br/>
  `/* Alterar a escala total do elemento */`<br/>
  `transform: scale(1.2);`<br/>
`}`<br/>
`#mais-vendidos li{`<br/>
  `/* Alterar a escala vertical e horizontal do elemento */`<br/>
  `transform: scale(1, 0.6);`<br/>
`}`
* Fonte: W3C, (2014).<br/>

####5.4 Skew<br/>

Distorce os elementos.<br/>
Quadro 16: Exemplo CSS, distorce os elementos selecionados.<br/>

`footer{`<br/>
  `/* Distorcer o elemento no eixo horizontal */`<br/>
  `transform: skewX(10deg);`<br/>
`}`<br/>
`#social{`<br/>
  `/* Distorcer o elemento no eixo vertical */`<br/>
  `transform: skewY(10deg);`<br/>
`}`
* Fonte: W3C, (2014).<br/>

Ainda pode-se combinar varias transformações no mesmo elemeto. O que deve-se fazer é declarar uma depois da outra. No quadro 17 podemos ver o exemplo.<br/>
Quadro 17: Exemplo CSS, combinando vários elementos<br/>

`html{`<br/>
  `transform: rotate(-30deg) scale(0.4);`<br/>
`}`
* Fonte: W3C, (2014).<br/>

###6.	Seletores avançados<br/>

####6.1 Seletor de irmãos<br/>

O quadro 18 apresenta um HTML que simula vários parágrafos, títulos e subtítulos em um documento.<br/>

Quadro 18: Exemplo HTML<br/>
`<article>`<br/>
  `<h1>Título</h1>`<br/>
  `<p>Início</p>`<br/>
  `<h2>Subtítulo</h2>`<br/>
  `<p>Texto</p>`<br/>
  `<p>Mais texto</p>`<br/>
`</article>`
* Fonte: Maujor, (2006).<br/>

Quadro 19: Exemplo CSS, seletor de irmãos<br/>
`h2 ~ p{`<br/>
  `font-style: italic;`<br/>
`}`
* Fonte: Maujor, (2006).<br/>

O seletor de irmãos (~) indica que queremos selecionar todos os `<p>` que foram precedidos por algum `<h2>` e são irmãos do subtítulo (ou seja, estão sob a mesma tag pai). <br/>

####6.2 Seletor de irmão adjacentes<br/>

Utilizando o HTML apresentado no quadro 18, quando se quer selecionar o paragrafo `<p>` e seguinte já existe um subtítulo `<h2>`, utilizamos o seletor de irmãos adjacentes.<br/>
Quadro 20: Exemplo CSS com seletor de irmão adjacentes<br/>
`h2 + p{`<br/>
  `font-variant: small-caps;`<br/>
`}`
* Fonte: Maujor, (2006).<br/>

Nesse caso apenas o texto será selecionado.<br/>

###7.	Text-shadow	<br/>

O text-shadow serve para colocar sombras em textos. Sua sintaxe é fácil de entender, recebe-se o deslocamento da sombra e a cor.<br/>

Quadro 21: Exemplo CSS, text-shadow<br/>
`p{`<br/>
  `text-shadow: 10px 10px red;`<br/>
`}`
* Fonte: W3C, (2014).<br/>

É possível até passar mais de uma sombra ao mesmo tempo para o mesmo elemento:<br/>
Quadro 22: Exemplo CSS, passando mais de uma sombra<br/>

`text-shadow: 10px 10px 5px red, -5px -5px 4px red;`
* Fonte: W3C, (2014).<br/>

###8.	Box-shadow<br/>

Podemos colocar sombras em qualquer elemento com o box-shadow, a sintaxe é parecida com a do text-shadow, deslocamento da sombra e a cor.<br/>

Quadro 23: Exemplo CSS com box-shadow<br/>
`box-shadow: 20px 20px black;`
* Fonte: W3C, (2014).<br/>

O box-shadow suporta mais um valor que faz a sombra aumentar ou diminuir, vejamos o exemplo no quadro 24<br/>
Quadro 24: Exemplo CSS<br/>
`box-shadow: 20px 20px 20px 30px black;`
* Fonte: W3C, (2014).<br/

###9.	Opacidade e RGBA<br/>

É possível mudar a opacidade de um elemento para que ele seja mais transparente com o uso da propriedade *opacity*. É simples, a propriedade *opacity* recebe um valor decimal entre 0 e 1, vejamos no quadro 25 o exemplo.<br/>
Quadro 25: Exemplo CSS, opacity<br/>

`p{`<br/>
  `opacity: 0.3;`<br/>
`}`
* Fonte: W3C, (2014).<br/>

Além das cores hexadecimais normais (#FFFFFF pro branco), podemos criar cores a partir de seu valor RGB, passando o valor de cada canal (Red, Green, Blue) separadamente (valor entre 0 e 255).<br/>
Quadro 26: Exemplo CSS, com todas equivalentes<br/>
`color: #FFFFFF;`<br/>
`color: white;`<br/>
`color: rgb(255, 255, 255);`
* Fonte: W3C, (2014).<br/>

Porém, existe uma função chamada RGBA que recebe um quarto argumento, o chamado canal Alpha. Na prática, seria como o *opacity* daquela cor (um valor entre 0 e 1), vejamos no quadro 27.<br/>
Quadro 27: Exemplo CSS, com a função RGBA<br/>
`/* branco com 80% de opacidade */`<br/>
`color: rgba(255,255,255, 0.8);`
* Fonte: W3C, (2014).<br/>
 
###10.	Gradientes<br/>
O CSS3 traz suporte a declaração de gradientes sem que se precise trabalhar com imagens, além de ser simples a página fica mais leve e a renderização fica melhor por se adaptar a todos os tipos de resolução. Existe suporte a gradientes lineares e radiais. No quadro 28 podemos ver melhor a sintaxe básica.<br/>
Quadro 28:Exemplo CSS de gradiente<br/>
`.linear{`
  `background: linear-gradient(white, blue);`<br/>
`}`<br/>
`.radial{`<br/>
  `background: radial-gradient(white, blue);`<br/>
`}`
* Fonte: Caelum, (2010)<br/>
 
No quadro 28 apresenta-se os exemplos dos tipos de gradientes lineares e radias, passando as cores branco (*white*) e azul (*blue*).<br/>
	Podemos ainda usar gradientes com angulações diferentes e diversas paradas de cores.<br/>
Quadro 29: Exemplo CSS com angulações diferentes<br/>
`.gradiente {`<br/>
  `background: linear-gradient(45deg, #f0f9ff 0%, #cbebff 47%, #a1dbff 100%);`<br/>
`}`
* Fonte: Caelum, (2010)<br/>
 
###11.	Foco<br/>

Coloca o foco no elemento quando ele for selecionado, no exemplo no quadro 30 apresenta o HTML normal, a única mudança ocorre no CSS.<br/>
Quadro 30: Exemplo HTML<br/>
`<input type="text">`
* Fonte: Caelum, (2010)<br/>

 	Veja que o HTML não muda, acima apresenta um simples input do tipo text, no quadro 31 apresenta o CSS referente ao quadro 30.<br/>
Quadro 31: Exemplo CSS, quando o foco está no input<br/>
`input:focus{`<br/>
    `background: yellow;`<br/>
    `border: 1px solid black;`<br/>
`}`
* Fonte: Caelum, (2010)<br/>
 
No quadro 31 apresenta que quando o foco está no input, à cor dele muda para amarelo (*yellow*), quando o foco sai do input a cor volta ao normal.
<br/>
###12.	Prefixos<br/>
Muitos dos novos recursos do CSS3 ainda são experimentais , isso quer dizer que foram incluídos nos rascunhos, mas ainda não são 100% oficias. As especificações ainda estão em aberto e vai demorar um pouco até serem finalizadas.<br/>
	Existem recursos mais estáveis e menos estáveis. Por outro lado, alguns são bem recentes e talvez ainda possa haver mudança até a aprovação final da especificação.<br/>
	Os navegadores desejam implementar os novos recursos antes mesmo da especificação terminar, para que os desenvolvedores possam começar a usar as novas propriedades e experimentá-las na prática. Entretanto, como a sintaxe final depois de aprovada pode ser diferente, os navegadores implementam as novas propriedades instáveis usando nomes provisórios.<br/>
	Uma boa pratica na utilização é pegar o nome da propriedade e colocar um prefixo na especifico do fabricante na frente. Quando a especificação ficar estável tira-se o prefixo e deixa-se a sintaxe oficial.<br/>
Os prefixos dos fabricantes mais usados são:<br/><br/>
Quadro 32: Prefixos dos fabricantes mais usados<br/>
**-webkit-**`: navegadores Webkit (Chrome, Safari, iOS, Android)`<br/>
**-moz-**`: Firefox (Mozilla)`<br/>
**-ms-**`: Internet Explorer (Microsoft)`<br/>
**-o-**`: Opera`
* Fonte: Caelum, (2010)<br/>
Quadro 33: Utilizando os prefixos no CSS<br/>
`p{`<br/>
  `/* Chrome até versão 3, Safari até versão 4 */`<br/>
  `-webkit-border-radius: 5px;`<br/>
  `/* Firefox até 3.6 */`<br/>
  `-moz-border-radius: 5px;`<br/>
  `/* Todas as versões modernas dos navegadores, `<br/>
   `incluindo IE e Opera que nunca precisaram de `<br/>
   `prefixo pra isso */`<br/>
  `border-radius: 5px;`<br/>
`}`
* Fonte: Caelum, (2010)<br/>
	No quadro 33 apresenta-se a utilização de prefixos utilizados no border-radius, fazendo com que o border-radius funcione em diversos navegadores, sem que sofra qualquer alteração.<br/>

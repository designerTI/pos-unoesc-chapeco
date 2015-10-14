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
*Fonte: Caelum, (2010)<br/>

###5.	Transforms


 




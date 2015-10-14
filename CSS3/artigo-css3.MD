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
	`<p>Mais textos de exemplos</p>`<br/> 
	
* Fonte: W3C, (2014).<br/><br/>

####CSS<br/>
Quadro 2: Exemplo CSS<br/>
`p{`<br/>
  `color: gray;`<br/>
`}`<br/>
`p.especial{`<br/>
  `color: black; /* cor do texto especial */`<br/>
`}`<br/>
* Fonte: W3C, (2014).<br/>

Outra forma de se fazer é com elementos que não batem naquela regra, isso quer dizer que, queremos todos os parágrafos que não têm a classe especial. A sintaxe do *:not()* recebe como argumento algum outro seletor simples como classes, id ou tags. Abaixo o exemplo.<br/>

####CSS<br/>
Quadro 3: Exemplo CSS :not()<br>
`p:not(.especial){`<br/>
  `color: gray;`<br/>
`}`<br/>

* Fonte: W3C, (2014).<br/>

###2.	Pseudo-classes <br/>
Quando se quer mudar a cor do primeiro e do ultimo elemento de uma lista, com elementos que já são pré definidos os elementos são chamamos de pseudo-classes. O primeiro elemento chamamos de *first-child* e o ultimo elemento de *last-child*. O HTML fica igual, vejamos o exemplo no quadro abaixo. <br/>



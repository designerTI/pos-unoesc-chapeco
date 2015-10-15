

###Atomic design<br/>

Ednilson Fernando Devilla<br/>
{marciano.guete@gmail.com}<br>

####Resumo<br/>
Neste artigo iremos abordar como funciona o Atomic design criado por Brad Frost, que através de analogias científicas, promete modificar a maneira de como organizamos e desenvolvemos interfaces.<br/>
####1) O que é?<br/>
É uma forma de pensar sobre o projeto que depende de componentes interligados, a partir de pequenas partes, que formam um todo organizado.<br/>
Em vez de olhar para os sites como um conjunto de páginas, você olha como um sistema de design, onde você divide em pequenos blocos que se juntam para eventualmente formar interfaces.

####2) Como funciona<br/>
Brad Frost utilizou metáfororas bastante conhecidas: átomos, moléculas, organismos, modelos e páginas.<br>
**Átomos:** são os elementos mínimos presentes em uma página.<br/>
**Moléculas:** Os átomos quando estão ligados em conjuntos formam moléculas. É a junção desses elementos em um padrão de interação que faça sentido para a pessoa que está usando.<br/>
**Organismos:** são grupos de moléculas, que se juntam para formar algo mais complexo.<br/> 
**Modelos:** consistem principalmente de grupos de organismos, os organismos juntos com os modelos formam as paginas. <br/>
**Paginas:** são onde os usuários passaram o seu tempo, também é onde testamos a eficácia do sistema de design.<br/> 

####3) Para que usar<br/>
Para se criar um padrão de código, que seja bem definido, de código limpo para facilitar a leitura e manutenção do código.<br/>
Os membros do time de design e do time do cliente conseguem visualizar melhor o sistema de design, sem necessariamente precisar ver todos os layouts salvos em .jpg em frente a eles.<br/>
Nesse formato, o sistema passa a ter maior escalabilidade. Você não está escolhendo breakpoints ou devices específicos para montar a sua interface, mas sim criando elementos que se comportam adequadamente a todos (ou quase todos) eles.<br/>
Para modularizar melhor a interface, criando ela desde o início responsivamente.<br/>
####4) Onde usar?<br/>
É usada para a criação de design de sistemas, geralmente esses sistemas são sites.<br/>

####5) Exemplos:<br/>
**Átomos:** são nossas tags do HTML, como um botão, um input, uma label ou ainda abstratos(animações, cores, fontes), que são invisíveis.<br>
**Moléculas:** quando se tem apenas um input ou apenas um botão, eles não podem fazer nada sozinhos, mas quando se juntam em um formulários (form), eles podem fazer algo juntos.<br/>
**Organismos:** Um organismo pode consistir de diversos componentes, como logotipo, navegação primaria, formulário de pesquisa, mas um organismo "lista de produtos" pode consistir da mesma molécula (possivelmente contendo uma imagem, o título e o preço do produto) repetindo uma ou varias vezes.<br/>
**Modelos:** Os modelos são os que fornecem contexto para todas as moleculas abstratas dos organismos. Os modelos são também onde os clientes começam a ver o desenho final no lugar.<br/>
**Paginas:** Através da página é possível ver todos os elementos menores como imagens e videos no contexto real e assim validar a efetividade do produto final após os ajustes<br/>

####Referência<br/>
* BLOOM, Chiristopher. Your Frontend Methodology Is All of Them: Atomic Design & Pattern Lab. 2014. Disponível em: <https://www.phase2technology.com/blog/your-frontend-methodology-is-all-of-them-atomic-design-patternlab>. Acesso em: 13 out. 2015.<br/>
* FROST, Brad. Atomic Desing. 2013. Disponível em: <http://bradfrost.com/blog/post/atomic-web-design/>. Acesso em 13 out. 2015.<br/>
* GUERRATO, Dani. O que é Design Atômico?. 2013. Disponível em: <http://tableless.com.br/o-que-e-design-atomic/>. Acesso em: 13 out. 2015.<br/>
* NASCIMENTO, Jean Carlo. Atomic Design - Por que usar?. 2014.  Disponível em: <http://nomadev.com.br/atomic-design-por-que-usar>. Acesso em: 13 out. 2015.<br/>
* ORTIZ, Mateus. Atomic Design como funciona. 2014. Disponível em: < http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/>. Acesso em: 13 out. 2015.<br/>
* TEIXEIRA, Fabricio. Atomic Design: redesenhando os entregáveis de designers e desenvolvedores. 2014. Disponível em: <http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/>. Acesso em: 13 out. 2015. <br/>

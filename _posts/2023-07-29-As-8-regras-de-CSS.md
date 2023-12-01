---
title: "As 8 regras de CSS"
date: 2023-07-29
---

# 🖋️ As 8 regras de CSS de Jarno Rantanen por Eduardo Rabelo

## Olá meus queridos leitores! 

Passei hoje para falar de algo relacionado ao que estamos vendo com o professor Abraão nestas semanas que passaram: Curiosidades sobre a linguagem CSS.

A curiosidade, que pode ser considerada dica, são 8 regras bacanas que [Eduardo Rabelo](https://medium.com/@oieduardorabelo) deixa bem explicado no seu [artigo](https://medium.com/tableless/8-regras-simples-para-uma-arquitetura-css-robusta-e-escal%C3%A1vel-545c6dade170) e vale a pena ler!



Bem, como eu não sei dar aula disso (ainda), vou postar as 8 regrinhas e uma breve explicação sobre elas. Cas você fique curioso e queira saber mais, dê um pulinho no link que deixei acima, blz? ;)

 
> 1 - Sempre prefira classes;

  <h6>Não use ID (ex: #header), porque, aonde você pensa que pode ter apenas uma instância de algo, em uma escala infinita, não vai dar certo. Com algumas exceções, seus estilos devem sempre usar classes.</h6>  
  </br>

> 2 - Mantenha os arquivos de um componente no mesmo lugar

  <h6>Quando estamos trabalhando em um componente, ajuda colocando tudo relacionado ao componente juntos. Ex:JS, CSS, testes, documentação, etc...</h6> 
        
        ui/
      ├── layout/
      |   ├── Header.js              // JS do componente
      |   ├── Header.scss            // CSS do componente
      |   ├── Header.spec.js         // testes do componente
      |   └── Header.fixtures.json   // se o teste precisar de mock
      ├── utils/
      |   ├── Button.md              // documentação
      |   ├── Button.js              // ...e por aí vai, você sacou
      |   └── Button.scss
      
</br>
 
> 3 - Use uma nomenclatura consistente
  <h6>Ele dá a dica de criar uma convenção de nomes e ficar usando essa convenção sempre, em todo o projeto. Por exemplo:</h6>
    
  <h5>O componente </h5> <h6>.myapp-Header-link.</h6> <h5>Cada uma das 3 partes desse nome tem um significado:</h5>
  
     **myapp** essa primeira parte serve para isolar nossa aplicação de outras que estiverem no mesmo DOM.
     **Header** essa parte serve para isolar nosso componente de outros componentes da nossa aplicação
     **link** é um nome local (dentro do escopo do nosso componente) para adicionar estilos a algo

<h6> "Sendo assim, o elemento principal do componente Header pode utilizar da classe myapp-Header. Para um componente simples, isso é tudo que você precisa.</h6>

<h6>Qualquer que seja a convenção de nome que você escolha, tem que ser consistente usando ela. Além de terem uma função, estas 3 partes querem significar algo. Apenas olhando para a classe, você já sabe aonde ela pertence. A nomenclatura deve ser o mapa que nos guia pela estrutura do projeto de dentro dos nossos estilos.</h6>

</br>

> 4 - Sempre use a mesma nomenclatura para nome de arquivos
 <h6>Essa é uma combinação lógica das duas regras anteriores (mantenha os arquivos de um componente no mesmo lugar, use uma nomenclatura consistente): Todos os arquivos que afetam um componente específico, devem conter o mesmo nome do componente. Sem exceção.</h6>  
      <div class=”myapp-Header”>…</div>
<h6>Daí quando começar a digitar "head..", vai aparecer:</h6>

![image](https://github.com/jmtannus/Blog-DC23/assets/61756665/6181725b-d425-4280-a92d-5423bdab77c7)

</br>

> 5 - Evite vazamentos de estilos para fora do componente
 <h6>Declarar o prefixo no início do seu arquivo. No exemplo abaixo, só precisou digitar o escopo uma única vez:</h6> 
      .myapp-Header {
        background: black;
        color: white;
      }
      .myapp-Header-link {
        color: blue;
      }
      .myapp-Header-signup {
        border: 1px solid gray;
      }
 <h5>Com essa abordagem, fica fácil usar nomes longos e únicos para classes, sem precisar se preocupar com a repetição da digitação desses nomes.</h5>

</br>

> 6 - Evite vazamentos de estilos dentro do componente
 <h6>Parece que prefixar um escopo único no nome da classe funciona muito bem para elementos vizinhos, mas não para elementos filhos.</h6> 
   <h5>Pode ser arrumado de duas maneiras:</h5> 
     <h6>1 - Nunca usar nomes de tag’s HTML nos nossos seletores. Se tudo dentro de Header for transformado em algo como <a class=”myapp-Header-link”>, nunca haverá problema. </h6> 
  <h5>Mas as vezes você tem sua marcação semântica criada da maneira correta, e não quer ficar adicionando classes nos elementos, nesse caso, vamos para a próxima opção:</h5> 
     <h6>2 - Usar o seletor de elementos filhos</h6>
       
      .myapp-Header {
        > a {
          color: blue;
        }
      }  
       
  </br>

> 7 - Respeito os limites do componente
 <h6></h6>  
  </br>

> 8 - Um modo mais simples de usar estilos externos
 <h6> Para evitar trabalho repetitivo, as vezes precisamos compartilhar estilos entre componentes. </h6>
 <h6> Para evitar isso completamente, de vez em quando procuramos estilos criados por outros. </h6>
 <h6> Ambas soluções devem ser alcançadas com o mínimo de acoplamento possível com sua base de código.</h6>
 <h6> Vamos usar Bootstrap como base para o nosso componente Button.</h6>
<h5> Ao invés de integrar pelo lado do HTML:</h5>
            
      <button class="myapp-Button btn">
      
<h5> Considere extender os estilos dessa classe:</h5>
      
      <button class="myapp-Button">
      .myapp-Button {
        // usando o Bootstrap
        @extend .btn;
      }
<h5> Isso reforça a idéia para todo mundo (inclusive você mesmo) de que os detalhes de implementação do <button> não precisam ser mostradas no HTML do componente.</h5>
<h5> Uma consequência boa disso, é que se você decidir trocar o Bootstrap por qualquer outro framework (ou simplesmente escrever o seu estilo próprio), a mudança ocorrerá apenas em uma parte.</button></h5>

</br>

   **Créditos:**
   <h5> *8 simple rules for a robust, scalable CSS architecture, originalmente escrito por Jarno Rantanen.*</h5> 
   <h5> *8 regras simples para uma arquitetura CSS robusta e escalável, artigo de Eduardo Rabelo para https://medium.com/*</h5> 

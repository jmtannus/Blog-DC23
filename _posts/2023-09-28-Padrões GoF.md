---
title: "Padrões GoF"
date: 2023-09-28
---

# Oba! Adoro! 🥰 Falando sobre Padrões de Projeto 🖋️

Vocês já ouviram falar de GoF (Gang of Four), ou seja, " a gangue dos quatro "?

São quatro caras top! --->  Erich Gamma, Richard Helm, Ralph Johnson e John Vlissides. 👨‍🦰🧔👨🏻👨🏽‍🦳

Eles publicaram um livro chamado: **Design Patterns: Elements of Reusable Object-Oriented Software.** em 1995 e, a partir daí , gerou-se um movimento ao redor de padrões de projeto. Mas eles não inventaram do zero os padrões de projeto! Dizem que veio bem antes, inspirado nos livros do arquiteto Christopher Alexander, publicados em 1977 a 1979.
Bem, mas disso a gente fala depois. Simbóra para os padrões GoF! Foco! kkkk

De acordo com o livro: "Padrões de Projeto: soluções reutilizáveis de software orientado a objetos", os padrões "GoF" são divididos em 24 tipos. Em função dessa grande quantidade de padrões, foi necessário classificá-los de acordo com as suas finalidades. São três classificações/famílias:

### 1ª : Padrões de Criação ou Criacionais

  >Os padrões criacionais fornecem vários mecanismos de criação de objetos, que aumentam a flexibilidade e reutilização de código já existente. Fornece uma interface para criar objetos em uma superclasse, mas permite que as subclasses alterem o tipo de objetos que serão criados.

- ***Abstract Factory***: capacidade de criar famílias de objetos on the fly com uma maior flexibilidade;
- ***Builder***: capacidade de construir o produto a partir de um passo-a-passo;
- ***Factory Method***: capacidade de criação de objetos on the fly com uma maior flexibilidade;
- ***Prototype***: permite que haja a criação de novos objetos a partir de uma cópia do modelo original ou um protótipo;
- ***Singleton***: permite a centralização de compartilhamento de recursos.

### 2ª : Padrões estruturais

  >Os padrões estruturais se preocupam com a forma como classes e objetos são compostos para formar estruturas maiores. Os de classes utilizam a herança para compor interfaces ou implementações, e  os de objeto descrevem maneiras de compor objetos para obter novas funcionalidades. A flexibilidade obtida pela composição de objetos provém da capacidade de mudar a composição em tempo de execução o que não é possível com a composição estática (herança de classes).

- ***Adapter***: essa funcionalidade possibilita o plugue do conteúdo em um sistema;
- ***Bridge***: possibilita a separação de implementações de abstrações em prol da flexibilidade;
- *Composite*: por meio dessa funcionalidade, é possível tratar todos os objetos de uma maneira justa;
- ***Decorator***: essa funcionalidade incrementa outras funcionalidades de uma maneira bem mais dinâmica;
- ***Façade (ou Facade)***: facilita a utilização de subsistemas considerados mais complexos;
- ***Business Delegate***: 
- ***Flyweight***: permite o compartilhamento de pequenos recursos visando economizar um pouco mais de espaço.
- ***Proxy***: o proxy faz com que um determinado objeto represente outro;

### 3ª : Padrões comportamentais

  > Conhecidos como **Behavioral Patterns**, Por meio desse tipo de produção é possível identificar padrões de comunicação que são comuns entre objetos e que podem ser capazes de dar continuidade aos padrões anteriormente estabelecidos.
  >Além disso, eles ainda são responsáveis por uma comunicação direta entre os objetos, principalmente no que diz respeito aos termos de responsabilidade e de algoritmo.

- ***Chain of Responsibility***: por meio dessa funcionalidade, há a possibilidade de repassar as requisições, evitando uma dependência entre um objeto e um determinado receptor e o solicitante. Dessa maneira, outros objetos que estão na mesma cadeira poderão ter a oportunidade de tratar essa determinada solicitação;
- ***Command***: capacidade de transformar requisições em objetos;
- ***Interpreter***: possibilidade de definir uma gramática e um interpretador;
-***Iterator***: capacidade de percorrer um determinado conjunto de dados, sem levar em consideração a sua implementação;
- ***Mediator***: capaz de simplificar os relacionamentos complexos;
- ***Memento***: possibilidade de externalizar estados sem, necessariamente, quebrar o encapsulamento;
- ***Observer***: possibilidade de realizar o compartilhamento de alguns recursos de uma forma mais inteligente;
- ***State***: pode ser considerado extremamente importante para simplificar a troca de estados internos de alguns objetos;
- ***Strategy***: possibilita a separação dos dados em algoritmos para que sejam reutilizados;
- ***Template Method***: define algoritmos com capacidade de extensão;
- ***Visitor***: determina uma nova operação para uma classe, mas sem alterá-la.

Existem outros critérios de classificação dos padrões de projeto:

**Finalidade**: reflete o que um padrão faz.
**Escopo**: especifica se o padrão é aplicado à classe ou objeto.

- Padrões com **escopo de classe**: utilizam a hierarquia para compor ou variar os objetos, mantendo a capacidade do sistema de se flexibilizar. Se realizarmos uma comparação com o outro tipo de classificação isso costuma acontecer quando se trata de um **padrão de criação**.

- Padrões com *escopo de objeto*: encontrados no relacionamento entre os objetos definidos em tempo de execução. Realizando uma comparação com o outro tipo de classificação vemos que esses padrões aparecem muito nos *padrões estruturais e comportamentais*.

## Mas tem gente que critica

 >Segundo alguns usuários, alguns "padrões de projeto" são apenas evidências de que alguns recursos estão ausentes em uma determinada linguagem de programação (Java ou C++ por exemplo). Nesta linha, Peter Norvig demonstra que 16 dos 23 padrões do livro 'Design Patterns' são simplificados ou eliminados nas linguagens Lisp ou Dylan, usando os recursos diretos destas linguagens.
 >Segundo outros, excessos nas tentativas de fazer o código se conformar aos 'Padrões de Projeto' aumentam desnecessariamente a sua complexidade.

É isso, pessoal estudioso! Vamos que vamos!

O que vocês achamram sobre essa "pincelada" sobre os padrões?

## Quer saber mais?

Gente, achei esse post muito massa, super educativo! Confere lá:
  > [!Design Patterns, Os Padrões do GOF](https://medium.com/@jonesroberto/desing-patterns-parte-2-2a61878846d) , escrito por *Jones Roberto*, CTO na Dezzot.

Obrigada por ler esse post até o final! Forte abraço! 🤗

[!fonte: be trybe](https://blog.betrybe.com/desenvolvimento-web/design-patterns-tudo-sobre/)

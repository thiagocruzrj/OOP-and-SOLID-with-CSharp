# Paradigma da Programação Orientada a Objetos
Seria uma abordagem que pensamos em termos do mundo real, ao invés de funções ou métodos.

Imagem : POO => Motorista, dinheiro, tanque
	    Procedural => Estacionar, Abastecer, Pagar

A programação procedural ou estruturada tem ênfase em sequência, decisão e iteração, ou seja, escrever procedimentos ou funções que executam operações em dados.
Já a programação orientada a objetos é um paradigma baseado no conceitos de dados, ou seja, a criação de objetos que contêm dados e métodos.
Sendo assim na POO nossa organização gira em torno de objetos e dados, ao invés de ações e procedimentos.

Imagem: POO x Programação Procedural

Assim podemos concluir que o grande objetivo da POO é refletir na estrutura do código a vida real do problema na qual o software busca resolver.

Existem inúmeras linguagens de suportam a POO, nesses artigos iremos falar sobre o C#, que é uma linguagem multiparadigmas ( tem suporte a outros tipos de visão que o programador sobre a estruturação e execução do programa ), tipagem forte ( exigência que o tipo de dado de um valor seja o mesmo tipo da variável quer o valor será atribuído ) e criado pela Microsoft fazendo parte da plataforma .NET.

Princípios básicos da POO

Encapsulamento:
Nos permite ocultar a implementação de uma classe do mundo externo.

Herança:
Permite que possamos herdar atributos e comportamentos de uma classe.

Polimorfismo:
Permite que um objeto se comporte de formas diferentes.

Abstração:
É o processo de identificação dos objetos e seus relacionamentos do mundo real.

Vantagens da POO em comparação com a programação estrutural:

Criação de códigos mais rápido e de fácil execução;
Fornece uma estrutura mais clara;
Pode se dizer que ajuda na manutenção, na escrita de códigos sólidos, modificação e depuração do código;  
Reuso de código e assim reduzindo o tempo de desenvolvimento.

Vantagens da programação estrutural em comparação a POO:
Provê um melhor controle sobre o fluxo de execução do código
Fácil compreensão, sendo assim muito usada em cursos introdutórios, já que tem um plano de sequência.  

Em resumo sobre a POO
Temos as classes objetos que permite a reusabilidade, já que com eles não precisamos copiar e colar o mesmo código em locais diferentes. Podemos assim criar uma classe e uma instância dessa classe após e reutilizar sempre que precisar.
Temos também a herança, composição e agregação que permite a extensibilidade. Imagine que temos uma função e você deseja entendê-la usando novos recursos podemos utilizar dos recursos acima para não ter que copiar todo o código.
Temos a simplicidade com a abstração, encapsulamento e o polimorfismo. Utilizado para que não tenhamos muitas funções e muito código disperso.

A fusão de todas essas características temos um projeto muito extensível, de fácil manutenção, sendo assim fácil de manter. Tornando assim a POO um dos paradigmas mais utilizado atualmente em inúmeras linguagens.

Classes e Objetos

Na linguagem C# tudo está ligado com classes e objetos, junto com seus comportamentos e atributos.

Um exemplo da vida real é um carro, ele é um objeto com atributos como marca, cor e potência, além de possuir comportamentos como acelerar e frear.
Para abstrairmos um carro em C# criamos uma classe com atributos e comportamentos e a partir dessa classe podemos criar objetos. Sendo assim uma classe nada mais é que um molde ou template para a criação de objetos, contendo em si os atributos e comportamentos que definem um objeto. Objetos não existem sem uma classe.

Imagem de uma classe em c#.

Em uma classe em c# podemos ter:
Campos: Nada mais é que uma variável declarada diretamente dentro de uma classe. Normalmente tem pouca visibilidade fora da classe.
Propriedades: Membro de uma classe com métodos específicos para o acesso de um campo que está escondido.
Construtores: É um criador e inicializador de objetos que ainda não existem, sendo chamados de forma implícita quando a palavra “new” cria um objeto, devem ter obrigatoriamente o mesmo nome da classe e não possuem retorno.
Métodos: Realizador de operações de objetos já criados, chamados diretamente quando um objeto for criado além de poder retornar algo ou não.

Construtores

Ao instanciar uma classe, ela por padrão, cria um construtor vazio e caso tenha propriedades ou campos nessa classe instanciada as tipagens feitas por referência (ex: string) é atribuído o valor null e as tipagens feitas por valor (ex: int) é atribuído o valor 0.
Também podemos criar construtores referenciado nossas propriedades ou campos como parâmetros, ou setar o valor de nossos campos ou propriedades dentro do construtor. 

Podemos ter mais de um construtor com parâmetros distintos, chamamos isso de sobrecarga. Assim como outros métodos, os construtores podem ser sobrecarregados usando diferentes números de parâmetros. Sendo assim, quando criamos dois métodos com o mesmo nome e parâmetros diferentes significa que estamos usando o recurso de sobrecarga.

Palavra reservada “This”

É a referência a instância atual da classe. Muito usada como o modificador do primeiro parâmetro de uma metodo de extensão.
Usamos muito para evitar a ambiguidade, ocultando membros com nomes semelhantes. Um exemplo seria o nome de propriedade uppercase parametrizada com uppercase em um construtor (qualificamos dessa forma this.Name = Name dentro do construtor); 
Passar um objeto como parâmetro para outros métodos; 
Como a palavra reservada “this” está vinculada a uma instância da classe ela não pode ser referir a um campo ou método estático ( Irei abordar modificadores de acesso na próxima sessão );

Modificadores de acesso

São os determinadores do nível de acesso para classes, campos, métodos e propriedades. Temos quatro modificadores de acesso e seis níveis de acessibilidade :

public : Sem restrição de acesso.
private : Restrito a membros da mesma classe;
protected: Restrito a membros da mesma classe e classes herdeiras.
internal: Restrita às classes dentro do projeto atual
protected internal: Herança restrita somente a classes do projeto atual;
private protected: Restrito a classe ou tipos derivados da classe que o contém no projeto atual;

FYI: Quando não há atribuição de modificador de acesso a classe por padrão o modificador é internal, já para membros da classe o modificador padrão é private;

Porque usamos Modificadores de acesso ?

Com eles temos os benefícios de controlar a visibilidade dos membros de uma classe além de obter o famoso "Encapsulamento" que nada mais é que a garantia que os dados "vulneraveis" sejam ocultados para outras classes, sendo que uma maneira de se obter essa restrição seria a declaração dos métodos de uma classe como private.

Propriedades e Encapsulamento

Encapsulamento

Nada mais é que o processo de esconder membros de uma classe do acesso exterior utilizando modificadores (Information hiding).
Um dos grandes benefícios seria a preservação da integridade da classe, ocultando detalhes importantes da implementação do mundo exterior.
A implementação é simples, temos o exemplo da declaração de membros (campos/variáveis) como privados além de também fornecer métodos públicos get e set (propriedades), para o acesso e atualização do valor de um campo privado.

Propriedade
Seria a combinação de variável e metodo, possuindo 2 métodos.

Ex: 
private string car;
public string Car {
	get { return car; }
	set { car = value; }
}

Nesse exemplo temos a propriedade Car associada ao campo car.
O método get retorno o valor do campo car.
O método set atribui um valor do campo car.

A palavra-chave value representa o valor atribuído à propriedade;


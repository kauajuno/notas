# Definição

O factory method é um design pattern que, dada uma interface para criar instâncias em uma superclasse, também torna possível que as subclasses criem tipos de objetos diferentes sem acoplar muito o código.

![[factorymethodclassdiagram.png]]

A interface produto declara uma interface a ser seguida por todos os produtos que poderão ser criados pelo creator, e assim os produtos fazem, sendo diferentes implementações do padrão Produto.

A classe Criador declara o Factory Method, que sempre retorna um Produto. Esse método pode ser declarado como abstrato para forçar que todos os criadores implementem sua própria versão, mas também pode ser implementada como um método default, que gera um produto default.

# Vantagens e desvantagens

O Factory Method é ótimo para ser usado de antemão quando não se sabe quais são as exatas dependências com as quais se vai trabalhar em um projeto. Também respeita os padrões SOLID, pois atribui a responsabilidade da criação de produtos a uma única classe e flexibiliza-a para possíveis mudanças que virão.

O código fica relativamente mais volumoso em razão da grande quantidade de subclasses que virão para cada novo produto.

---

#designpattern #creationalpattern

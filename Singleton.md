# Definição

Singleton é um design pattern que assegura que uma classe tenha uma única instância em tempo de execução do programa. Isso pode ser desejado em aplicações multithread nas quais só pode existir uma conexão de determinado tipo simultaneamente, por exemplo, em um banco de dados.

![[singletonclassdiagram.png]]

# Vantagens e desvantagens

Não existe bem como citar uma vantagem no Singleton que não seja o de ele cumprir muito bem o seu propósito. Ele só gera a instância quando ela ainda não existe e garante um ponto de acesso global para aquela instância.

Entretanto, ultimamente as desvantagens do Singleton tem ficado bem claras. Além de violar o princípio de responsabilidade única, classes Singleton são muito difíceis de cobrir em testes
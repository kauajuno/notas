

EM CONSTRUÇÃO


# Laços de repetição

Ainda falando em estruturas de controle, elas existem para resolver problemas que inviabilizariam a codificação se elas não existissem. Se não houvesse o if-else, não haveria código, pois não seria possível manter vários fluxos de controle e todos os programas teriam uma "árvore de fluxos" completamente linear.

Agora, imagine uma ação repetitiva, que precisa ser realizada várias e várias vezes. Por exemplo, suponhamos que eu quero um código que faça "Tic" para um segundo e "Tac" para o segundo seguinte, durante dez segundos. O código ficaria enorme, mas ainda seria possível fazer isso, de certa forma.

```php
echo "Tic";
sleep(1);
echo "Tac";
sleep(1);
echo "Tic";
sleep(1);
echo "Tac";
sleep(1);
echo "Tic";
sleep(1);
echo "Tac";
sleep(1);
echo "Tic";
sleep(1);
echo "Tac";
sleep(1);
echo "Tic";
sleep(1);
echo "Tac";
```

Agora imagine que quiséssemos fazer isso durante uma hora inteira, que tem 3600 segundos. Claro, é apenas uma situação hipotética, mas um código como esse não seria prático de se fazer de forma alguma, as mesmas 4 linhas de código teriam que se repetir 1800 vezes.

Para lidar com estruturas repetitivas assim existem os laços de repetição, cuja função é repetir uma mesma tarefas quantas vezes for necessário até que uma condição estabelecida seja satisfeita, interrompendo a repetição.

- `while`: checa se uma condição está satisfeita e, se estiver, executa o bloco de código compreendido em seu escopo. O processo se repete enquanto a condição for satisfeita.
- `do while`: lógica semelhante ao `while`, mas em vez de checar a condição primeiro e executar depois, ele executa primeiro e checa a condição depois. Isso garante que o código será executado ao menos uma vez.
- `for`: esse laço possui três elementos principais, que são a inicialização, a condição de parada e o incremento. Na inicialização, ele inicializa uma variável no escopo do laço. Na condição de parada, é estabelecida uma condição assim como nos dois laços apresentados anteriormente, que executará o bloco de código se for satisfeita. No incremento, alguma variável é incrementada.
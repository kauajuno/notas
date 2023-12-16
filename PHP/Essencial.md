# Variáveis

Variáveis em PHP são declaradas com o símbolo `$`. Sempre é necessário atribuir um valor a uma variável quando instanciada em PHP, mesmo que esse valor seja `null` . Como PHP é uma linguagem não tipada, o tipo fica implícito no código, mas eles ainda existem, os tipos primitivos em PHP são: string, integer, double, boolean e NULL. Seguem uma variável de cada um dos tipos mencionados nessa respectiva ordem.

```php
$nome = "Kauã Júnio";
$idade = 21;
$saldo = 90.99;
$estudando = true;
$variavelNula = null;
```

# Operações matemáticas

```php
$idade = 21 + 2;
// $idade == 23
$idade += 2;
// $idade == 25
$idade -= 2;
// $idade == 23
$idade = $idade * 2;
// $idade == 46
$idade = $idade / 2;
// $idade == 23;
$idade = 2;
$idade = $idade ** 3;
// $idade == 8 (2 ao cubo)
$idade = $idade % 2;
// $idade == 0 (resto da divisão por 2)
```

# Strings

A string em PHP é um dos tipos primitivos que possui uma gama de funções nativas para lidar com operações comuns a serem realizadas com strings. Primeiramente, existem diversas formas de se declarar uma variável do tipo string.

```php
$aspassimples = 'Sou uma string';
$aspasduplas = "Também sou uma string";
$heredoc = <<<EOT pode parecer estranho, mas também sou uma string EOT;
$nowdoc = <<<'EOT' e eu também sou uma string EOT;
```

Strings podem ser concatenadas para formarem outras strings:

```php
$cumprimento = "Olá! ";
$quemsoueu = "Meu nome é Kauã";
$frasecompleta = $cumprimento . $quemsoueu;
echo $frasecompleta;
// Olá! Meu nome é Kauã
```

A concatenação pode ser útil para colocar dados de variáveis dentro de uma string.

```php
$idade = 21;
echo 'Ola, eu tenho ' . $idade . 'anos.';
```

Porém, tenha em mente que isso não é necessário quando aspas duplas são utilizadas:

```php
$idade = 21;
echo "Ola, eu tenho $idade anos.";
```

Existem caracteres especiais em PHP, que quando invocados realizam algum tipo de ação especial. Os exemplos mais comuns disso são o de quebra de linha e o TAB.

```php
echo "\tNessa linha houve um TAB.\nNessa não houve."
//     Nessa linha houve um TAB.
// Nessa não houve.
```

> [!info]
> Usar a constante PHP_EOL é mais recomendado do que usar o caractere de quebra de linha \\n. Isso acontece pois diferentes sistemas operacionais podem usar diferentes caracteres especiais para representar ações diferentes, o PHP_EOL é uma constante que universaliza a ação da quebra de linha para que o comportamento seja idêntico em qualquer SO.


# Condicionais

As condicionais em PHP funcionam da mesma forma que na maioria das outras linguagens de programação: é uma estrutura de controle que altera o fluxo de execução do programa com base em uma condição. Se a condição especificada por verdadeira, ela executa o bloco de código que vem em seguida. Também é possível especificar um bloco de código para ser executado caso a condição não seja satisfeita, com uma estrutura if-else.

```php
$aprovado = true;

if($aprovado){
	echo "Parabéns, você foi aprovado!";
}else{
	echo "Infelizmente você foi reprovado!";
}

// Parabéns, você foi aprovado!
```

Condicionais podem ficar cada vez mais complexas, apresentando múltiplos caminhos (else if) e condicionais aninhadas.

```php
$aprovadoPorNota = true;
$aprovadoPorPresenca = true;
$comportado = true;

if($aprovadoPorPresenca){
	if($aprovadoPorNota){ // condicional aninhada, uma dentro da outra
		echo "Você foi aprovado, parabéns!";
	}
}else if($comportado){ // else if
	echo "Seu bom comportamento lhe rendeu uma segunda chance.";
}else{
	echo "Melhore seu comportamento!";
}
```

>[!info]
>É importante evitar condicionais aninhadas se possível, pois prejudica exponencialmente a legibilidade do código.
# Operadores

Operadores geram expressões que retornam um valor booleano. Existem operadores unários e binários.

## Operadores unários

Operadores unários funcionam sobre um único valor, formando uma expressão composta pelo operador e pelo valor. A operação binária mais comum é a de negação, que transforma um valor booleano no seu valor oposto.

```php
$vivo = true;
$vivo = !$vivo;
// vivo == false
```
## Operadores binários

Operadores binários funcionam sobre dois valores. Seguem expressões com os operadores binários mais comuns.

```php
$val1 = 15;
$val2 = 30;

$v1maiorquev2 = $val1 > $val2; // false
$v1menorquev2 = $val1 < $val2; // true
$v1igualav2 = $val1 == $val2; // false
$v1maiorouigualav2 = $val1 >= $val2; // false
$v1menorouigualav2 = $val1 <= $val2; // true
$v1diferentedev2 = $val1 != $v2; // true
```

Operadores binários também podem ser usados em tipos de variáveis que não sejam inteiros.

A utilização mais comum desses operadores são em condicionais.

```php
$usuario = "Joao";

if($usuario == "Joao"){
	echo "Seja bem-vindo $usuario";
}else{
	echo "Quem é você?";
}
```

# Mais estruturas condicionais

De fato a estrutura de controle condicional mais comum é a do if-else, mas ainda existem outras duas em PHP: `switch` e `match`.

O `switch` é uma estrutura de controle com uma popularidade não muito favorável: ela é restrita e verbosa. Restrita pois compara uma única variável com um conjunto de múltiplos valores, impossibilitando comparações mais complexas. Verbosa pois de fato, para cada condição adicionada, as linhas de código aumentam consideravelmente.

```php
$day = date('D');

switch ($day) {
  case 'Mon':
    echo "It's Monday. Back to the grind!";
    break;
  case 'Tue', 'Wed', 'Thu':
    echo "Another weekday. Keep on hustling!";
    break;
  case 'Fri':
    echo "TGIF! Time to unwind and relax.";
    break;
  case 'Sat', 'Sun':
    echo "Weekend time! Enjoy your day off!";
    break;
  default:
    echo "Invalid day!";
    break;
}
```

>[!info]
>A função `date` utilizada acima é relativamente simples: no bloco de código acima, ela recebe um parâmetro que especifica o formato que será retornado, que nesse caso foi 'D', que significa 'Day', e vem em forma abreviada. O retorno da função no caso é basicamente o dia da semana do momento em que o código for executado. No dia em que essa anotação está sendo escrita, 16/12/2023, o retorno seria 'Sat'.

Já o `match` tem um carinho a mais dos desenvolvedores. Apesar de também ser uma estrutura de controle restrita em relação às comparações, ela é muito menos verbosa do que a estrutura mencionada anteriormente.

```php
$fruit = "apple";

$message = match ($fruit) {
  'apple', 'orange' => "A healthy choice!",
  'banana' => "Great source of potassium!",
  default => "Enjoy your fruit!",
};

echo $message;
```

# Laços de repetição

Os laços de repetição presentes em PHP são `while`, `do while`, `for` e `foreach`.


```php

```
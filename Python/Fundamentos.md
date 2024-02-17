# PEPs

Antes de ir pra qualquer aspecto mais a fundo da programação algo muito importante sobre a linguagem de programação que a fez melhorar conforme os anos foram passando são as PEPs, acrônimo para Python Enhancement Proposals. As PEPs podem ser acessadas [aqui](https://peps.python.org/pep-0000/). 

Uma das PEPs mais importantes é a [PEP8](https://peps.python.org/pep-0008/). Ela fornece um guia de estilo para código python, algo desejado em praticamente toda linguagem de programação. É desejado que todos os códigos apresentem aspectos similares para facilitar legibilidade.

Seguem algumas práticas indicadas:

- Identação deve ser feita usando 4 espaços (TAB não serve).
- O tamanho máximo de uma linha deve ser de 79 caracteres.
- Quebra de linha em expressões, se necessária, deve vir antes de operadores binários.
- Classes e funções definidas globalmente devem ser cercadas por duas linhas em branco.
- Definições de métodos dentro de classes devem ser cercadas por uma linha em branco.
- A última linha de um arquivo .py deve terminar em branco.
- Cada import deve ocupar apenas uma linha por biblioteca referenciada.
- Imports sempre devem ser colocados ao topo do arquivo, antes de módulos globais e constantes, porém depois de comentários de módulo e docstrings.
- Nomes de funções e variáveis devem ser sempre em letras minúsculas usando underlines para separar o nome se necessário.
- Nomes de classes devem usar letras capitalizadas.

Entre muitas outras indicadas.

Mas aí tem muita coisa nova também. Tipo, o que é uma docstring? Mais pra frente chegaremos lá.

# Variáveis e tipos de dados

Sendo uma linguagem dinamicamente tipada, em Python não é necessário atribuir o tipo da variável de antemão.

Existem diferentes tipos de dados, seguem eles:

- Numéricos
	- int
	- float
	- complex
- Booleanos
	- bool
- Sequências
	- list
	- tuple
	- range
- Sequências de texto
	- str
- Tipos de sequência binária
	- bytes
	- bytearray
	- memoryview
- Tipos de conjunto
	- set
	- frozenset
- Tipos de mapeamento
	- dict

São muitos tipos, e na verdade não são todos, somente os mais utilizáveis e compreensíveis. Mas se ainda não deu pra entender tudo bem, vamos ter uma visão top-down fácil de entender.

- [[Python/Tipos Numéricos]]
- 

# Introdução

O software hoje é algo que está em praticamente todo lugar. É algo que aceitamos como fato sem refletirmos muito sobre, mas quando paramos para prestar atenção, o software de fato está em todos os lugares hoje em dia. No sistema do supermercado onde fazemos compras, na geladeira onde guardamos comidas e bebidas, no celular que acessamos diversas vezes ao dia, nos aplicativos que utilizamos para nos comunicar, nos veículos que nos conduzem. A verdade é que é difícil olhar para uma direção e não identificar um software em utilização naquela cena.

Por isso, com o crescimento massivo da utilização do software, o software se tornou uma indústria, com uma ampla gama de áreas de aplicação: jogos, comércio, saúde, redes sociais, etc.. E de todas as maneiras também, sendo softwares de sistema, softwares de aplicativo, softwares embarcados, software de banco de dados, e assim por diante. Fato é que, sendo algo tão disseminado no mundo, o software profissional deve seguir um padrão de excelência. Os quatro parâmetros principais para isso são:

- Manutenibilidade: o software deve ser criado de forma que esteja aberto para evoluções.
- Confiança e proteção: o software deve saber lidar com adversidades/falhas do sistema sem comprometer os dados com que lida, bem como não permitir acesso não autorizado aos dados.
- Eficiência: o software deve usar os recursos do sistema eficientemente e sem desperdício.
- Aceitabilidade: o software deve ser aceito pelo seu público alvo, isto é, deve ser algo com que o público alvo não tenha dificuldades para lidar e, idealmente, já estejam familiarizados com aquilo.

De fato são muitos tipos de software, várias áreas de aplicação e várias formas pelas quais ele pode aparecer. Surge então uma questão: a abordagem clássica da engenharia de software é capaz de conduzir a construção de qualquer tipo de software? Essencialmente, sim. Como assim essencialmente? Bom, essencialmente, as principais etapas da construção do software são:

- Compreender o problema
	- Qual é o cerne do problema?
	- Quem está interessado nisso?
	- É possível dividir esse problema?
	- Existe uma solução?
	- Como se pode representá-lo?
- Planejar uma solução
	- Já houveram problemas semelhantes?
	- Como esses problemas foram resolvidos?
	- É possível dividir esse problema? (mais uma vez)
	- Como se representa a solução?
- Executar o plano
	- A solução construída é de fato adequada?
	- Todas as partes estão corretas?
	- As partes do software estão de fato coesas entre si?
- Examinar o resultado
	- Como testar a solução?
	- Os resultados dos testes são satisfatórios?

# Categorização de software

No capítulo anterior, foram listadas poucas categorias de software, como os embarcados, os de aplicação, e etc. Não existe um padrão universal de como se categorizar software. Diferentes autores na engenharia de software categorizam os softwares de maneira diferente.

Em 2016, Pressman listou 6 categorias de software:

- Software de Sistema: programa feito para atender outros programas, como compiladores, sistemas de gerenciamento de arquivos/notas, etc.
- Software de Aplicação: programas independentes que processam operações comerciais ou administrativas.
- Software de Engenharia/Administrativo: programas que realizam cálculos massivamente, como os utilizados em astronomia ou engenharia civil (AutoCAD).
- Software Embarcado: executa funções limitadas e extremamente específicas. Por exemplo, o software de um micro-ondas, uma geladeira ou de uma câmera de segurança.
- Software para Linha de Produtos: oferece capacidade específica para uma gama de clientes que podem personalizar partes do software.
- Aplicações Web/Aplicativos Móveis: aplicações executadas em navegadores ou dispositivos móveis.
- Software de IA: usa algoritmos não numéricos para solucionar problemas complexos.

Wazlawick, por sua vez, já tinha visualizado outra maneira de se categorizar software:

- Software Básico: softwares de auxílio para outros softwares.
- Software de Tempo Real: softwares que gerenciam atividades que estão acontecendo em tempo real, como softwares de gerenciamento de tráfego.
- Software Comercial ou Sistemas de Informação: sistemas aplicados em empresas.
- Software Científico ou Software de Engenharia: utilizam processo intensivo de números.
- Software Embarcado: equivalente ao de Pressman.
- Software Pessoal: softwares office, leitores de arquivos e outros softwares comuns utilizados amplamente no dia-a-dia.
- Jogos: autoexplicativo.
- Inteligência Artificial: sistemas especialistas, redes neurais e sistemas com capacidade de aprendizado.

Outra classificação muito interessante é a de Forward, de 2008:

- Software predominante em dados
	- Software orientado a consumidor
	- Software orientado a negócio
	- Software de engenharia e design
	- Software de exibição de informação e entrada de transação
- Software de sistema
	- Sistemas operacionais
	- Networking
	- Dispositivos/Periféricos
	- Utilidades
	- Middleware
	- Backplanes (ex: IDEs)
	- Servidores
	- Malware
- Software predominante em controle
	- Controle de hardware
	- Software embarcado
	- Software de controle em tempo real
	- Software de controle de processo
- Software predominante em computação
	- Pesquisa de operação
	- Manipulação e gerenciamento de informação
	- Criatividade artística
	- Software científico
	- Inteligência artificial

Observando todas essas diferentes formas de se classificar um software, é possível notar pequenas diferenças em detalhes de classificação e um grau maior ou menor de especificação, mas existem certos "sensos comuns" quanto a classificação.

Retomamos então, de uma maneira diferente, a questão levantada no capítulo anterior. A abordagem de engenharia de software utilizada para cada uma dessas categorias de software podem ser IGUALMENTE aplicadas? A essência de fato permanece para todas as categorias, mas diferentes categorias exigem sim abordagens diferentes, mesmo que sejam ligeiramente diferentes.

Softwares embarcados, por exemplo, vão requerer uma abordagem que enfatize a eficiência da utilização de recursos do sistema, ao passo que software de entretenimento (plataformas de streaming, por exemplo), vão requerer um foco em UX/UI que nem sequer é utilizado em softwares embarcados.

# Engenharia de Sistemas vs. Engenharia de Software

Ao longo dos estudos em Engenharia de Software, é possível perceber o atrelamento dela com a Engenharia de Sistemas. Mas vamos definir melhor essas fronteiras: o quão relacionadas essas engenharias são? O quão influente uma é na outra? Uma contém a outra? Ou são independentes, apesar de relacionadas?

## O que é sistema e o que é software

Sistemas é uma coleção intencional de componentes relacionados de diferentes tipos, que quando trabalham em conjunto são capazes de oferecer um conjunto de serviços ao seu utilizador. Todas as partes do sistema são essenciais para o seu funcionamento completo.

Um software é um conjunto de componentes lógicos que compõem um programa que pode ser executado em algum dispositivo.

## Relação sistema-software

Esses dois são mais fáceis de se relacionar quando se olha para as camadas que cada uma abrange. A engenharia de sistemas lida com a organização em questão, seus processos de negócio, as aplicações utilizadas dentro da organização, as comunicações e gerenciamento dos dados dessas aplicações, os sistemas operacionais sobre os quais essas aplicações operam (infraestrutura), e por fim os equipamentos físicos nos quais esses OSs rodam. Já a engenharia de software cobre alguma dessas camadas, por estar envolvida na idealização, construção e manutenção dos aplicativos, precisando portanto estar ciente dos processos organizacionais e dos sistemas sobre os quais as aplicações rodam.

## A camada sociedade

Existe ainda uma camada acima da organização, que é a sociedade, que representa todos os princípios éticos e morais e as leis que regem o Estado no qual a organização está sedeada. Portanto a Engenharia de Sistemas não está isolada, já que, apesar de não conseguir influenciar na camada da sociedade ela é influenciada por ela.

A sociedade influencia ambas as engenharias, e a engenharia de sistemas influencia a engenharia de software.




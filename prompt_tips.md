# Possíveis características de um bom prompt.

* Busca características de reprodutibilidade.
* Direciona o chat diretrizes de texto.

*Exemplo 1 (Conclusão)*:
```
Me dê um título para uma promoção de jogo de futebol.

Compre seu novo jogo...
```
*Exemplo 2 (Few Shots)*:
```
Quero criar uma única troca de falas entre dois personagens.

Exemplo 1: Olá, tudo bem?
Resposta 1: Sim e você?

Exemplo 2: Está chovendo bastante não é?
Resposta 2: Você acha? Não percebi.

Exemplo 3: No que você estava pensando?
Resposta 3: Até parece que você faria melhor.

Exemplo 4: Qual sua cor favorita?
Resposta 4: 
```

* Ordem no início ("Eu quero, eu preciso, me dê...").
* Itens da resposta desejada pré-definida.
* Demandas quebradas em pequenas tarefas.
* Texto de saída formatado.

*Exemplo 3 (formato em código)*:

```
...

Devolva o resultado em código Javascript:

` ` `
parâmetro 1 = ""
parâmetro 2 = ""
parâmetro 3 = ""
parâmetro 4 = ""
parâmetro 5 = ""
lista 1 = []
lista 2 = []
lista 3 = []
` ` `
```
> Para quem programa, isso pode ser utilizado para automatizar processos. Podem pedir dados de entrada e fazer com que o chat GPT apresente os dados de saída.

* *Exemplo 4 (formato em formulário)*

```
...

Devolva o resultado no seguinte formato:

parâmetro 1 = _______
parâmetro 2 = _______
parâmetro 3 = _______
parâmetro 4 = _______
parâmetro 5 = _______
lista 1 = _______;_______;_______;_______.
lista 2 = _______;_______;_______;_______.
lista 3 = _______;_______;_______;_______.

```

* Modelo de saída reforçado (*faça SOMENTE...; retorne APENAS...*)
* Delimitadores inclusos.

>  """ (três aspas duplas): O uso de três aspas duplas é comum em várias linguagens de programação e serve para indicar um texto que não deve ser processado ou interpretado. No ChatGPT, isso pode ser usado para >separar o texto da instrução. Isso ajuda a deixar a intenção da pergunta ou tópico mais clara para o modelo, facilitando a geração de uma resposta.
>
> Exemplo:
>
```
Dê um título para o texto abaixo:

Texto:

“””Python é uma linguagem de propósito geral de alto nível, multiparadigma, suporta o paradigma orientado a objetos, imperativo, funcional e procedural. Possui tipagem dinâmica e uma de suas principais características é permitir a fácil leitura do código e exigir poucas linhas de código se comparado ao mesmo programa em outras linguagens. “””

Título:
```

> [```] três crases: As três crases são usadas para indicar que o conteúdo entre elas é tratado como um bloco de código.

> _____ (sublinhados): Os sublinhados podem ser usados para gerar um resultado no formato de formulário. Isso é interessante, caso você queira automatizar o resultado de um prompt e não deseja que o resultado seja em código, apenas em texto.

* Pontuação, acentos e caracteres especiais bem aplicados.
* Contexto do prompt bem explicado.
* Perguntas simples e diretas.
* 

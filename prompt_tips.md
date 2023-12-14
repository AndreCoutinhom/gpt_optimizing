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

* 

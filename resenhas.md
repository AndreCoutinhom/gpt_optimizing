# Desafio: analisando sentimentos em várias resenhas

Uma empresa que fabrica air-fryers está interessada em entender as opiniões das pessoas consumidoras sobre o desempenho do produto e as suas funcionalidades. A empresa deseja o seguinte para cada resenha:

* Um resumo em português com no máximo 30 palavras;
* Uma lista com os pontos fortes do aparelho;
* Uma lista com os pontos fracos do aparelho;
* O sentimento final da pessoa em relação ao produto, ou seja, se o sentimento é positivo, neutro ou negativo.

Sua tarefa será analisar as seguintes resenhas de pessoas que compraram o produto em uma loja online americana.

* Resenha 1: I use the air fryer a lot. It works very well. I made hamburgers in it last night, the were wonderful! The rack you put the food on is a little hard to clean. It has lots of crevices that food gets in. The basket itself is very easy to clean. I also do not trust the rack not to fall out when dumping out food, like French fries.

* Resenha 2: Air fryer works fine until the handle breaks off. There's only 3 screws that attach the handle to a plastic piece on the basket. The plastic piece breaks and the screws fall out so there's no way to attach the handle to the basket rendering the air fryer useless. If there were 4 screws or if the screws attached to metal the handle attachment would have been much more secure and less prone to breaking.

* Resenha 3: Even though I returned it for the bigger one of the same company I liked the fryer. Ferry ez to use But hard to judge. Seafood button isn't fish and it was a guessing game how to cook the product. I way over cooked it and the chicken legs came out crispy, but the other side was raw. But, this is my first time using an air fryer so maybe it's me. Very sleek on the counter buttons light up real nice. I made tater tots and let me tell you they came out perfect and stayed hot. I like it so much that I returned this one and got the same company Bigger one. But I had to buy it from the place itself not from Amazon and I don't lie that at all. Hope this review helps.

Além disso, será necessário gerar um resultado no formato de saída JSON, para que os dados sejam utilizados para análises posteriores. Neste arquivo JSON, você precisa especificar que quer 5 chaves:

* ID da resenha
* Resumo
* Lista de pontos fortes
* Lista de pontos fracos
* Sentimento

Com base nas respostas a essas perguntas, a empresa poderá identificar oportunidades de melhoria em seu produto e aprimorar sua estratégia de marketing.

---

## Prompt

```
Considere as seguintes resenhas de compras online:

**Resenha 1:** "I use the air fryer a lot. It works very well. I made hamburgers in it last night, the were wonderful! The rack you put the food on is a little hard to clean. It has lots of crevices that food gets in. The basket itself is very easy to clean. I also do not trust the rack not to fall out when dumping out food, like French fries."

**Resenha 2:** "Air fryer works fine until the handle breaks off. There's only 3 screws that attach the handle to a plastic piece on the basket. The plastic piece breaks and the screws fall out so there's no way to attach the handle to the basket rendering the air fryer useless. If there were 4 screws or if the screws attached to metal the handle attachment would have been much more secure and less prone to breaking."

**Resenha 3:** "Even though I returned it for the bigger one of the same company I liked the fryer. Ferry ez to use But hard to judge. Seafood button isn't fish and it was a guessing game how to cook the product. I way over cooked it and the chicken legs came out crispy, but the other side was raw. But, this is my first time using an air fryer so maybe it's me. Very sleek on the counter buttons light up real nice. I made tater tots and let me tell you they came out perfect and stayed hot. I like it so much that I returned this one and got the same company Bigger one. But I had to buy it from the place itself not from Amazon and I don't lie that at all. Hope this review helps.".

Faça uma leitura dessas resenhas e me retorne uma resposta para cada resenha com os seguintes parâmetros:

""" 
Resumo em português (máximo de 30 palavras): XXXX;
Lista com pontos fortes do produto: [Y; Y; Y; Y];
Lista com pontos fracos do produto: [Z; Z; Z; Z];
Sentimento único do consumidor: positivo / misto / neutro / negativo;

"""

O retorno deve ser trazido seguindo os seguintes parâmetros:

"""
Formato: JSON
Chaves: 
- ID da resenha: _____
- Resumo: XXXX
- Lista de pontos fortes: [Y; Y; Y; Y]
- Lista de pontos fracos: [Z; Z; Z; Z]
- Sentimento: _____
"""
```

## Resposta do chat

``` json
{
  "ID da resenha": 1,
  "Resumo": "Air fryer funciona muito bem para fazer hambúrgueres, mas a grade é difícil de limpar devido às fendas. Desconfiança quanto à estabilidade ao despejar alimentos.",
  "Lista de pontos fortes": ["Eficiência no cozimento"],
  "Lista de pontos fracos": ["Dificuldade de limpeza da grade", "Possível instabilidade da grade ao despejar alimentos"],
  "Sentimento": "Misto"
}

```

``` json
{
  "ID da resenha": 2,
  "Resumo": "Air fryer funciona bem, mas a alça é propensa a quebrar devido à fragilidade da peça de plástico. Reforçar a alça com mais parafusos ou material metálico seria benéfico.",
  "Lista de pontos fortes": ["Desempenho geral"],
  "Lista de pontos fracos": ["Fragilidade da peça de plástico na alça", "Número insuficiente de parafusos na alça"],
  "Sentimento": "Negativo"
}

```

``` json
{
  "ID da resenha": 3,
  "Resumo": "Apesar dos desafios iniciais, o consumidor aprecia a facilidade de uso e design atraente. Algumas dificuldades na compreensão dos botões, mas a satisfação global levou à troca por um modelo maior.",
  "Lista de pontos fortes": ["Facilidade de uso", "Design atraente", "Bom desempenho com tater tots"],
  "Lista de pontos fracos": ["Confusão nos botões", "Desafios ao cozinhar alguns alimentos"],
  "Sentimento": "Positivo"
}

```

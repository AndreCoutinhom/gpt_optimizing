# Entendendo o que são tokens

Já deu pra notar que projetar seu prompt é essencialmente como você “programa” o modelo, geralmente fornecendo algumas instruções ou alguns exemplos. Mas como esse modelo funciona? Como ele sabe o que vai nos responder?

Os modelos entendem e processam o texto dividindo-o em tokens. Um token pode ser uma palavra individual, um caractere, ou até mesmo uma parte de uma palavra. Por exemplo, a frase “Hello World!” teria os seguintes tokens:

![image](https://github.com/AndreCoutinhom/gpt_optimizing/assets/91290799/85295b6b-89fe-4eb7-94b3-6cae9e2f3a95)

Temos 3 tokens:

* Hello;
* world e;
* um token para o sinal de exclamação.

Enquanto isso, essa mesma frase em português, seria dividida da seguinte forma:

![image](https://github.com/AndreCoutinhom/gpt_optimizing/assets/91290799/739b3b4a-2c55-465e-b89a-4582d460ab91)

Nesse caso temos 5 tokens:

* Ol;
* á;
* mund;
* o e;
* um token para o sinal de exclamação.

Com isso, é possível verificar que dependendo do idioma o processo de tokenização divide as palavras de forma diferente.

Se você tiver curiosidade em checar como um texto se traduz em tokens, existe uma ferramenta da OpenAI chamada [tokenizer](https://platform.openai.com/tokenizer).

O modelo do ChatGPT atribui um valor de representação a cada token, capturando informações contextuais e semânticas. Essas informações semânticas referem-se ao significado e à interpretação das palavras, frases ou sentenças em um contexto específico.

A semântica está relacionada ao estudo do significado das palavras e como elas se combinam para formar ideias e expressões mais complexas.

No contexto do processamento de linguagem natural, as informações semânticas são usadas para capturar o significado e a intenção subjacentes a uma sequência de palavras. Ao entender as informações semânticas, um modelo de linguagem como o ChatGPT pode inferir o contexto e responder de maneira mais precisa.

Então, os tokens de entrada são passados sequencialmente pelo modelo, permitindo que ele analise o contexto anterior para gerar previsões sobre o próximo token.

É importante mencionar que o número de tokens de entrada é limitado para garantir o bom desempenho do modelo e controlar os custos computacionais. Se um prompt exceder o limite de tokens permitido, será necessário reduzi-lo ou dividir em partes para se adequar ao limite.

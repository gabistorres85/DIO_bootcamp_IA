# Análise de linguagem Natural por meio de PLN

Objetivo - entender os fundamentos básicos de PLN e como aplicar algorítimos para diferentes tipos de situações.

## PLN 

- redes de Deep Learning, para reconhecer a voz.

- além de entender as palavras precisa entender a semântica da frase. 

- grande área da computação com IA. 

- PLN é uma vertende da IA que ajuda a computadores a entender, interpretar e manipular a linguagem humana.

## Assistente virtual 

- uma aplicação de LPN

- Sistema de reconhecimento e comando por voz. 

## Níveis do processamento

- análise em forma de pirâmide 

1. Morfologia - utilizada para o reconhecimento de voz.
2. Syntax - entender a palavra e sua  pontuação. Contexto de palavras parecidas.
3. Semântica - o sentido de palavra pode ser diferente dentro de um contexto. 
4. Pragmáticaa - ramo da linguística que estuda a linguagem no contexto de seu uso na comunicação. 

## Deep Learning para PLN

### Sistema de interpretação de linguagem natural

- depende de um treinamento de cada palavra e cada contexto, para transcrever e converter para processamento computacional.

- considerar aspectos: como contexto de conversa, sistemas sisntáticos e semmânticos, interpretação de textos e análise de sentimentos.

### Redes de Deep Learning

 Os primeiro modelos usavam arquitetura NN feedforward ou NN convolucional, mas não capturava muito bem o contexto. Para melhorar esse aspecto foram aplicados NNs recorrentes.

O LSTM, uma variedade do RNN para capturar o contexto de longa fistância. O LSTM bidirecional melhora o LSTM ao observar as sequências de palavras nas direções para frente e para trás. 

O google substitui seu sistema de tradução baseado em frase pela Neural Machine Translation (NMT). Isso reduz os erros de tradução em +0%. Ele usa uma rede LSTM profunda com 8 camadas de codificador e 8 de decodificador. - interpretar cada palavra, depois analisar o contexto.

- revolução na área de NLP com DL iniciou em 2018, com odelos de linguagem pré-treinados ELMo e ULMFit. 
Após veio a Transformer, mecanismos de atenção. Permiti o treinamento com número maior de dados. Desenvolveu-se um modelo de linguagem pré-treinado, um sistema treinamento previammente e submetido a um treinamento com ajuste fino (fine-tuning) nas tarefas específica da liguagem.

Word Embeddings são representações vetorias das palavras, que permitem captutar o contexto e relacionamento das palavras nos documento, sem an ecessidade de realizar engenharuia de features com anotações exaustivas nas setenças. Utiliza a proximidade cartesianas entre as palavras.

ImageNEt em 2012 - iniciou o interesse de pesquisadores no mundo todo por Deep Leraning.

2018 - rev na área de NLP - ELMo, GPT e BERT.

## Exemplo prático de PLN

Códgio Python:

### Biblioteca utilizadas: 

- speech_recognition - bibiblioteca com funções de speech to text
- os - para comunicar com o sistema operacional.

- com essa biblioteca é possível identificar palavras para realizar alguns comandos simples.

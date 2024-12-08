# Visão computacional

- Baseada na IA
- Capturar imagem nas câmeras e entender ela
- discriminar nas imagens o que são esses objetos. 
- reconhecimento facil, a partir das características de um rosto.
- Posicionamento da câmera
- Detectar objetos em imagens
- Classificação da imagem 
- classificação + localização = detecção; aplicada em algorítimos para detectar pesssoas e automóveis, placas.

- Detecção de objetos em imagens: detecção de caracterísitcas, primeiro passo é simplificar a imagem para apenas as bordas, para retirar as cores e texturas. 

As bordas entram na classificação da rede neural e vários dados são coletados, espaço entre os olhos, cor de pele, espaço entre sobrancelhas

Extração de features automáticas dois sistemas: 

Neural network não tem tantos recursos de neuronios
Deep Learning : maior capacidade de reconhecimento. 

1º tem a avaliação por partes e por fim o rosto como todo. 

Estruturas de rede

[Playground TensorFlow](https://playground.tensorflow.org) - ambiente para treinamento de redes neurais com exmeplos práticos.

## Dataset

Criando sua base de dados - é preciso contornar cada rosto e dizer quem é quem. 

## Rastreamento de objetos


### Introdução 

Algoritmos de Tracking de imagens: acompanhamento do movimento da imagem, influencia o reconhecimento da imagem ser a mesma pessoa e o fim da ação. Identificação de cada objeto com um rótulo, por exemplo. Assim identifica que aquele objeto é um mesmo objeto.

não basta reconhecer as imagens, é necessário interpretar.

Rede Yolo identifica as pessoas, mas não rotula cada um.

Rede Yolosort identifica e rastreia os objetos.

## Rede para Rastreamento em Imagens

algumas aplicações possíveis: 
- carros autônomos
- contagem de animais na agriculutra
- controle de pragas

Segmentação de imagens: separa os objetos por tipos, mas não consegue identificar o que é cada agente
Agente - objetos que se move e interagem com nosso ambiente. Base para tomada de decisões.

### Tipos de redes pra Tracking e imagens

#### Yolo Sort

Rede detecta o objeto e rastreia em função do tempo. Tem uma divisão temporal, cada frame é avaliado em relação ao frame autal, passado e prevê a presença dele no frame futuro. Implementação fácil é rápida.

Aplicado na área de segurança - verificar comportamentos suspeitos.
Acompanhamento em provas virtuais.

#### Mask-RCNN

Aplicação mais robusta que a Yolo Sort. Rede de segmentação, identifica e segmenta os objetos, facilita a percepção do acompanhamento do movimento. Para identificar o acompanhamento dos agentes, predizendo o futuro através dos frames presentes em comparação com o passado.

### Rede Yolo Sort

Rede Yolo - trabalha com detecção e rastreamento de objetos, grande potencial para detecção de objetos em grande volume de imagens simultâneas. Arquitetura a custo baixo, atualmente versão 7. consegue rodar no celular. consegue ser utilizada em hardwares de baixzo processamento. Realiza uma varredura na imagem, coloca em bouding box em cada objeto.

Yolo Sort - Gera a possibilidade de rastreamento em função do tempo. acompanhamento ao longo do tempo em curto e médio prazo.s

Baseado em LSTM - Long Short Term Time- avaliação de tempo em curto e longo prazo. 
avalia um objeto em um frame e outro - curto prazo  - detecção de velocidade, por exemplo. 

avalia um objeto em=ntre vários frames - longo prazo 

arquitetura - primeiro detecta o objetivo, depois estima a velocidade e rota do objeto. 

Algortimo

1. transforma o vídeo em vários frames


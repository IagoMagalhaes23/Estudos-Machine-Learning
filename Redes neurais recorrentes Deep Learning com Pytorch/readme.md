# Redes neurais recorrentes: Deep Learning com Pytorch

## Introdução
Esse curso é sobre redes neurais recorrentes, que são o tipo de rede neural adequada para você trabalhar com dados sequenciais.

### Aula 01
- O que é a memória de sequência.
    A memória humana ao processar sequências não memoriza elementos individuais, mas, sim, o padrão que relaciona os elementos em uma determinada ordem. Redes neurais recorrentes (RNN) foram projetadas com o mesmo propósito.

- Tipos de dados sequenciais
    Quaisquer conjuntos de dados onde cada amostra pode ser dividida em eventos individuais, sendo a ordem dos eventos um fator relevante. Por exemplo: texto, voz, partitura musical, vídeo etc.

- Limitações do Multi-Layer Perceptron (MLP)
    Apesar de ser possível aplicar o MLP no processamento de sequências, ele apresenta uma série de limitações em grande parte relacionadas à sua incapacidade de memorizar acontecimentos passados.

- Motivação para o uso de Redes Neurais Recorrentes
    As limitações do MLP levaram à proposição de uma nova arquitetura, a RNN, capaz de guardar uma memória interna de acontecimentos passados, levando-os em consideração ao processar novos eventos.

### Aula 02
- O fluxo de dados em uma célula recorrente.
    A célula recorrente básica possui muitas similaridades com um Multi-Layer Perceptron, com a vantagem extra de uma memória interna que permite acumular contexto dos elementos de uma sequência em um processamento iterativo.

- RNNCell no PyTorch
    O pacote nn de redes neurais do PyTorch fornece uma célula recorrente simples, que nos permite implementar explicitamente o fluxo iterativo de uma sequência.

- A memória interna (hidden state)
    A memória interna de uma RNN básica nada mais é do que um vetor do mesmo tamanho que a quantidade de neurônios da camada. Ela recebe esse nome por ser retroalimentada para a camada, acumulando contexto da sequência.

- Construção de Vocabulário e Representação One Hot
    No contexto de processamento de texto, aprendemos a representar strings como tensores, modelando uma sequência de caracteres a partir de um vocabulário pré-definido.

- Classificação de nomes com uma Char-RNN
    Nossa primeira prática! Aqui você viu como usar a RNNCell processando nomes próprios como uma sequência de caracteres para predizer a sua nacionalidade.

### Aula 03
- Taxonomia dos problemas
    Dependendo dos dados utilizados e inferências desejadas, a sua arquitetura recorrente pode tomar as seguintes formas: Many-to-One, One-to-Many, Many-to-Many e Many-to-Many sincronizado. Por exemplo, a análise de sentimentos é um problema Many-to-One.

- Vanishing Gradient
    O problema do gradiente que desaparece (ou explode) é especialmente importante para modelos recorrentes, se considerarmos que sequências muito longas produzem um processamento “profundo” no tempo.

- O uso de Gates
    Os portões (gates) são parte essencial dos métodos que solucionam o problema do vanishing gradient. Aqui você viu como eles se aplicam a uma feature passando pela célula recorrente.

- LSTM e GRU
    Também chamadas de células recorrentes avançadas, a LSTM e a GRU são as principais células capazes de processar longas sequências, mitigando o problema do vanishing gradient.

## Referências
- [Redes Neurais Recorrentes:
Deep Learning com Pytorch](https://www.alura.com.br/curso-online-rnn-redes-neurais-recorrentes-deep-learning-pytorch)
- [Notebook 01](https://caelum-online-public.s3.amazonaws.com/1892-redes-neurais-recorrentes-deep-learning-pytorch/02/Classifica%C3%A7%C3%A3o%20de%20Sequ%C3%AAncias.ipynb)
- [Versão animada do fluxo de dados nas unidades recorrentes](https://towardsdatascience.com/animated-rnn-lstm-and-gru-ef124d06cf45)
- [função dos gates da LSTM](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [Conheça a principal referência quando se fala em RNNs](https://karpathy.github.io/2015/05/21/rnn-effectiveness/)
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

## Referências
- [Redes Neurais Recorrentes:
Deep Learning com Pytorch](https://www.alura.com.br/curso-online-rnn-redes-neurais-recorrentes-deep-learning-pytorch)
- [Notebook 01](https://caelum-online-public.s3.amazonaws.com/1892-redes-neurais-recorrentes-deep-learning-pytorch/02/Classifica%C3%A7%C3%A3o%20de%20Sequ%C3%AAncias.ipynb)
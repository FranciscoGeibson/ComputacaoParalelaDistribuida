# Ordenação de Vetores com Threads (8 Threads)

Este repositório apresenta um programa em C++ que realiza a ordenação de vetores com o uso de *8 threads*, implementando divisão de trabalho e paralelismo para otimizar o desempenho.

## Descrição do Programa

O programa executa as seguintes etapas em um vetor de tamanho fixo:

1. Preenche o vetor com valores aleatórios.
2. Divide o vetor em *8 partes* iguais, cada uma designada a uma thread.
3. Ordena cada parte do vetor usando a função std::sort em paralelo.
4. Mede os tempos de preenchimento, ordenação e execução total.

## Características

- *Divisão de Trabalho*:
  - O vetor é particionado em partes iguais, processadas simultaneamente por 8 threads.
- *Paralelismo*:
  - Uso de pthread para gerenciamento de threads.
- *Análise de Desempenho*:
  - O programa calcula e exibe os tempos para preenchimento, ordenação e execução total.

## Requisitos

- Compilador compatível com C++11 ou superior.
- Biblioteca pthread (Linux nativo ou equivalente no Windows, como Cygwin/MinGW).

## Compilação e Execução

### Compilar o Programa

Use o seguinte comando para compilar o código:

```bash
g++ -o ordenacao_threads_8 ordenacao_threads_8.cpp -pthread
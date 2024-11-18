# Ordenação de Vetores com Threads

Este repositório contém um programa em C++ que realiza a ordenação de vetores utilizando múltiplas threads, demonstrando divisão de tarefas e processamento paralelo. Ele preenche um vetor com valores aleatórios, divide em partes iguais e utiliza threads para ordenar simultaneamente.

## Funcionalidades

- *Preenchimento do vetor*:
  - Preenche o vetor global com valores aleatórios usando std::srand.
- *Divisão do vetor*:
  - Divide o vetor em partes iguais para processamento paralelo.
- *Ordenação com múltiplas threads*:
  - Cada thread ordena sua parte do vetor usando std::sort.
- *Medição de tempos*:
  - Tempo de preenchimento, ordenação e execução total.

## Requisitos

- Compilador C++ compatível com C++11 ou superior.
- Biblioteca pthread (Linux, ou adaptadores no Windows como Cygwin/MinGW).

## Como Usar

### Compilação

Para compilar o programa, utilize o comando:

```bash
g++ -o ordenacao_threads ordenacao_threads.cpp -pthread
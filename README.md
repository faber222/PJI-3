# Laboratórios Didáticos para Ensino de Sistemas de Comunicação em FPGA

Este repositório contém os materiais do Projeto Integrador 3 (PJI3) do curso de Engenharia de Telecomunicações do IFSC-SJ. O projeto propõe o desenvolvimento de laboratórios didáticos em FPGA voltados ao ensino de sistemas de comunicação digital.

O objetivo principal é aproximar a teoria e a prática, permitindo aos estudantes implementar e testar blocos fundamentais de comunicação (como modulação, codificação e OFDM) diretamente em hardware, complementando a formação teórica.

## Blocos Implementados (Estudo de Caso LTE)

Com base em um levantamento de requisitos e seguindo as especificações, os blocos fundamentais escolhidos para implementação foram:

1.  **Modulação QPSK (Quadrature Phase Shift Keying):**
    * **O que é:** Uma técnica de modulação digital que mapeia pares de bits em símbolos complexos (I+jQ), alterando a fase da portadora para transmitir dois bits por símbolo. É amplamente utilizada em cenários de baixa relação sinal-ruído.
    * **Material Teórico:** `ARQUIVOS-DIDATICOS/Modulação-QPSK-e-sua-aplicação.pdf`

2.  **Codificação Turbo (Turbo Coding):**
    * **O que é:** Um código corretor de erros (FEC) de alto desempenho, conhecido por sua capacidade de se aproximar do Limite de Shannon. No padrão LTE, é implementado como um PCCC (Parallel Concatenated Convolutional Code) com taxa de 1/3, garantindo robustez contra erros de transmissão.
    * **Material Teórico:** `ARQUIVOS-DIDATICOS/Codificação Turbo e sua aplicação.pdf`

3.  **OFDM (Orthogonal Frequency Division Multiplexing):**
    * **O que é:** A base para tecnologias como Wi-Fi, 4G e 5G. É uma técnica de modulação que divide o fluxo de dados em múltiplas subportadoras ortogonais. Isso torna o sistema robusto contra interferência intersimbólica (ISI) causada por multicaminho e permite alta eficiência espectral.
    * **Material Teórico:** `ARQUIVOS-DIDATICOS/Modulação OFDM e sua aplicação.pdf`

## Conteúdo do Repositório

* `PlanoDeTrabalhoPJI3.pdf`: O plano de trabalho completo do projeto, detalhando objetivos, metas, cronograma e equipe.
* `M1/`: Documentação da Meta 1 (Análise de Requisitos), incluindo o relatório de análise do questionário e o relatório de definição dos blocos LTE.
* `ARQUIVOS-DIDATICOS/`: Apresentações teóricas que explicam os conceitos fundamentais de cada bloco (QPSK, Turbo, OFDM).
* `TUTORIAIS/`: Guias práticos passo a passo para a implementação.
* `LICENSE`: Licença MIT do projeto.

## Fluxo de Trabalho (Tutorial QPSK)

O arquivo `TUTORIAIS/Tutorial-Modulação-QPSK-e-sua-aplicação.pdf` detalha o fluxo de trabalho completo para modelar, simular e gerar o VHDL para o modulador QPSK.

### Tecnologias Utilizadas

* **Modelagem e Simulação:** MATLAB + Simulink
* **Geração de Código:** HDL Coder (do MATLAB)
* **Síntese e Implementação:** Quartus Prime (Intel/Altera FPGA)
* **Verificação de Hardware:** ModelSim

### Passos Principais do Tutorial

1.  **Modelagem em Simulink:** O tutorial guia a criação de um modelo Simulink para o modulador QPSK, usando fontes de sinal (seno, cosseno), um gerador de sequência e o bloco "QPSK Modulator Baseband".
2.  **Simulação (Simulink):** Demonstra como executar a simulação no Simulink e visualizar os sinais de entrada e a saída modulada (com as mudanças de fase) em um Time Scope.
3.  **Geração de VHDL (HDL Coder):** Mostra como usar o "HDL Workflow Advisor" no MATLAB para selecionar o subsistema `qpsk`, configurar os parâmetros e gerar o código VHDL e o testbench sintetizáveis.
4.  **Projeto no Quartus Prime:** Instruções para criar um novo projeto no Quartus, adicionar os arquivos VHDL gerados pelo HDL Coder e compilar o design.
5.  **Simulação (ModelSim):** O tutorial finaliza mostrando como executar os scripts de compilação (`.do`) no ModelSim para verificar o comportamento do código VHDL, confirmando que a saída do hardware corresponde à simulação.

## Equipe

* Faber Bernardo Júnior
* Jamilly da Silva Pinheiro
* Jéssica Gomes Carrico

## Licença

Este projeto está licenciado sob a Licença MIT.

Copyright (c) 2025 Faber Bernardo
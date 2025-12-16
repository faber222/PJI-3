# Laboratórios Didáticos para Ensino de Sistemas de Comunicação em FPGA

Este repositório contém os materiais do Projeto Integrador 3 (PJI3) do curso de Engenharia de Telecomunicações do IFSC-SJ. O projeto propõe o desenvolvimento de laboratórios didáticos em FPGA voltados ao ensino de sistemas de comunicação digital.

O objetivo principal é aproximar a teoria e a prática, permitindo aos estudantes implementar e testar blocos fundamentais de comunicação (como modulação, codificação e OFDM) diretamente em hardware, complementando a formação teórica.

## Blocos Implementados

Com base em um levantamento de requisitos e seguindo as especificações, os blocos fundamentais escolhidos para implementação foram:

1.  **Modulação QPSK (Quadrature Phase Shift Keying):**
    * **O que é:** Uma técnica de modulação digital que mapeia pares de bits em símbolos complexos (I+jQ), alterando a fase da portadora para transmitir dois bits por símbolo. É amplamente utilizada em cenários de baixa relação sinal-ruído.
    * **Material Teórico:** [Modulação QPSK e Sua Aplicação](./ARQUIVOS-DIDATICOS/Modulação-QPSK-e-sua-aplicação.pdf)

2.  **Codificação Turbo (Turbo Coding):**
    * **O que é:** Um código corretor de erros (FEC) de alto desempenho, conhecido por sua capacidade de se aproximar do Limite de Shannon. No padrão LTE, é implementado como um PCCC (Parallel Concatenated Convolutional Code) com taxa de 1/3, garantindo robustez contra erros de transmissão.
    * **Material Teórico:** [Codificação Turbo e Sua Aplicação](./ARQUIVOS-DIDATICOS/Codificação-Turbo-e-sua-aplicação.pdf)

3.  **OFDM (Orthogonal Frequency Division Multiplexing):**
    * **O que é:** A base para tecnologias como Wi-Fi, 4G e 5G. É uma técnica de modulação que divide o fluxo de dados em múltiplas subportadoras ortogonais. Isso torna o sistema robusto contra interferência intersimbólica (ISI) causada por multicaminho e permite alta eficiência espectral.
    * **Material Teórico:** [Modulação OFDM e Sua Aplicação](./ARQUIVOS-DIDATICOS/Modulação-OFDM-e-sua-aplicação.pdf)

## Conteúdo do Repositório


```text
.
├── ARQUIVOS-DIDATICOS
│   ├── Codificação-Turbo-e-sua-aplicação.pdf
│   ├── Modulação FSK e sua aplicação.pdf
│   ├── Modulação-OFDM-e-sua-aplicação.pdf
│   └── Modulação-QPSK-e-sua-aplicação.pdf
├── LICENSE
├── M1
│   ├── DefinicaoBlocosLTE.pdf
│   ├── Laboratórios Didáticos para Ensino de Sistemas de Comunicação em FPGA.pdf
│   ├── PlanoDeTrabalhoPJI3.pdf
│   ├── Questionario.PJI3.pdf
│   └── RELATORIO-PJI3-QUESTIONARIO (2).pdf
├── M2
│   └── Laboratórios Didáticos para Ensino de Sistemas de Comunicação em FPGA_M2.pdf
├── M3
│   └── Laboratórios Didáticos para Ensino de Sistemas de Comunicação em FPGA (1).pdf
├── README.md
└── TUTORIAIS
    ├── fsk
    ├── ofdm
    ├── qpsk
    └── turbo
```

### Tecnologias Utilizadas

* **Modelagem e Simulação:** MATLAB + Simulink
* **Geração de Código:** HDL Coder (do MATLAB)
* **Síntese e Implementação:** Quartus Prime (Intel/Altera FPGA)
* **Verificação de Hardware:** ModelSim

### Passos Principais do Tutorial

1.  **Modelagem em Simulink** 
2.  **Simulação (Simulink)** 
3.  **Geração de VHDL (HDL Coder)** 
4.  **Projeto no Quartus Prime**
5.  **Simulação (ModelSim)**
6.  **Gravação na DE2-115**

## Equipe

* Faber Bernardo Júnior
* Jamilly da Silva Pinheiro
* Jéssica Gomes Carrico

## Licença

Este projeto está licenciado sob a Licença MIT.

Copyright (c) 2025 Faber Bernardo

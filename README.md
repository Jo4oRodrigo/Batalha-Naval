# Batalha-Naval

Este projeto em **C** implementa um tabuleiro de batalha naval simplificado, onde é possível aplicar diferentes **habilidades especiais** (Cone, Cruz e Octaedro) em um campo de batalha.  
Cada habilidade afeta posições específicas no tabuleiro, permitindo simular padrões de ataque em jogos de estratégia.

---

## Funcionalidades

- Criação de um **tabuleiro 10x10** com:
  - `0` → Água
  - `3` → Navio
  - `5` → Área afetada por habilidade
- Definição de três tipos de habilidades:
  - **Cone** → Expande em formato triangular.
  - **Cruz** → Afeta linhas e colunas a partir de um ponto central.
  - **Octaedro (Losango)** → Afeta células em formato de diamante.
- Impressão no console de **um tabuleiro para cada habilidade**, mostrando o impacto no campo de batalha.
- Organização modular com funções para inicializar, aplicar e imprimir o tabuleiro.

---

## Estrutura do Código

- `inicializarTabuleiro` → Preenche o tabuleiro com água (`0`).
- `posicionarNavio` → Insere navios fixos no tabuleiro (`3`).
- `imprimirTabuleiro` → Exibe o tabuleiro no console.
- `aplicarHabilidade` → Sobrepõe a matriz de habilidade no tabuleiro.
- `criarCone`, `criarCruz`, `criarOctaedro` → Geram matrizes 7x7 representando os padrões de ataque.

---

## Exemplo de Saída no Console
```
### 🔺 Tabuleiro com habilidade **CONE**

0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0
0 0 0 0 5 5 5 0 0 0
0 0 0 5 5 5 5 5 0 0
0 0 5 5 3 3 5 5 0 0
0 0 0 5 3 3 5 0 0 0
0 0 0 0 5 5 5 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0

### ✝️ Tabuleiro com habilidade **CRUZ**
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 5 3 3 5 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0
0 0 0 0 0 5 0 0 0 0

### 💠 Tabuleiro com habilidade **OCTAEDRO**
0 0 0 0 0 0 0 0 0 0
0 0 0 0 5 0 0 0 0 0
0 0 0 5 5 5 0 0 0 0
0 0 5 5 5 5 5 0 0 0
0 0 5 5 3 3 5 0 0 0
0 0 0 5 3 3 5 0 0 0
0 0 0 5 5 5 0 0 0 0
0 0 0 0 5 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0
```
---

## ⚙️ Como Compilar e Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/Batalha-Naval.git
   cd tabuleiro-habilidades
Compile o programa:

bash
Copiar
Editar
gcc main.c -o batalhaNaval
Execute:

bash
Copiar
Editar
./batalhaNaval

📜 Licença
Este projeto é distribuído sob a licença MIT.
Sinta-se livre para usar, modificar e compartilhar.

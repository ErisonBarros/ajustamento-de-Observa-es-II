---
description: Prof. Erison Barros
---

# Introdução ao Método dos Mínimos Quadrados

## Introdução ao Método dos Mínimos Quadrados

O método dos mínimos quadrados (MMQ) é uma técnica matemática amplamente utilizada na geodésia e em diversas áreas científicas para ajustar dados observados e estimar parâmetros desconhecidos. Ele minimiza o impacto de erros de medição, proporcionando estimativas confiáveis.

***

### Motivação do Método dos Mínimos Quadrados

* **Problema**: Observações frequentemente apresentam erros e inconsistências devido à redundância ou incertezas nas medições.
* **Objetivo**: Determinar uma solução que minimize os efeitos desses erros, ajustando os dados observados.

***

### Definição Matemática

O problema pode ser representado por:

$$
\mathbf{y} = \mathbf{A}\mathbf{x} + \mathbf{e}
$$

Onde:

* **A : Matriz de design (m×nm \times nm×n)**
  * Representa as relações lineares entre as observações e os parâmetros desconhecidos.
  * Suas dimensões m×nm \times nm×n indicam que há mmm observações e nnn parâmetros desconhecidos.
  * Geralmente, é composta por coeficientes que ligam cada parâmetro desconhecido a cada equação de observação.
* **x : Vetor de parâmetros desconhecidos (n×1n \times 1n×1)**
  * Contém as variáveis que queremos determinar.
  * É um vetor coluna com nnn elementos, onde nnn é o número de parâmetros a serem estimados.
* **e: Vetor de resíduos (m×1m \times 1m×1)**
  * Representa as discrepâncias entre os valores observados e os ajustados (modelados).
  * Suas dimensões m×1m \times 1m×1 correspondem ao número de observações.

O objetivo é minimizar a soma dos quadrados dos resíduos S:

$$
S = \mathbf{e}^T \mathbf{e} = (\mathbf{y} - \mathbf{A}\mathbf{x})^T (\mathbf{y} - \mathbf{A}\mathbf{x})
$$

***

### Resolução pelo MMQ

Para minimizar (S), derivamos em relação a (\mathbf{x}) e igualamos a zero:

$$
\frac{\partial S}{\partial \mathbf{x}} = -2\mathbf{A}^T(\mathbf{y} - \mathbf{A}\mathbf{x}) = 0
$$

Isso resulta na **equação normal**:

$$
\mathbf{A}^T\mathbf{A}\mathbf{x} = \mathbf{A}^T\mathbf{y}
$$

A solução para (\mathbf{x}) é:

$$
\mathbf{x} = (\mathbf{A}^T\mathbf{A})^{-1}\mathbf{A}^T\mathbf{y}
$$

***

### Propriedades do Estimador de MMQ

1. **Estimativa não tendenciosa**:
   *   O valor esperado de E é igual ao parâmetro real, assumindo que o modelo é correto:

       $$
       \mathbb{E}[\mathbf{x}] = \mathbf{x}_{\text{real}}
       $$
2. **Variância mínima**:
   * Entre os estimadores lineares não tendenciosos, o MMQ possui a menor variância.
3. **Covariância do estimador**:
   *   A matriz de covariância do estimador é:

       $$
       \text{Cov}(\mathbf{x}) = (\mathbf{A}^T\mathbf{A})^{-1}\sigma^2
       $$

       Onde (\sigma^2) é a variância das observações.

***

### Aplicações Práticas

* **Ajuste de redes geodésicas**: Determinação de coordenadas em redes de nivelamento, triangulação e GNSS.
* **Modelagem de superfícies**: Ajuste de curvas e superfícies baseadas em dados observados.
* **Análise de resíduos**: Identificação de discrepâncias nos dados observados.

***

### Exemplo Simplificado

#### Problema: Ajustar uma linha reta (y = mx + c) a dados observados ((x\_i, y\_i)).

**Matriz de design**:

$$
\mathbf{A} = 
\begin{bmatrix}
x_1 & 1 \\
x_2 & 1 \\
\vdots & \vdots \\
x_n & 1
\end{bmatrix}
$$

**Vetor de observações**:

$$
\mathbf{y} = 
\begin{bmatrix}
y_1 \\
y_2 \\
\vdots \\
y_n
\end{bmatrix}
$$

**Vetor de parâmetros**:

$$
\mathbf{x} = 
\begin{bmatrix}
m \\
c
\end{bmatrix}
$$

**Solução**:

$$
\mathbf{x} = (\mathbf{A}^T\mathbf{A})^{-1}\mathbf{A}^T\mathbf{y}
$$

***

O método dos mínimos quadrados é essencial para obter soluções confiáveis em problemas com dados redundantes e medições com incertezas.

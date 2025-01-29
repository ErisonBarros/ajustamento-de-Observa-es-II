---
icon: pencil
---

# Exemplo: Aplicação do Método Correlato em uma Rede de Nivelamento

### Descrição do Problema

Considere uma rede de nivelamento composta por quatro pontos (A), (B), (C) e (D) e quatro desníveis observados:

1. $$h_{AB}$$: Desnível de (A) para (B),
2. $$h_{BC}$$: Desnível de (B) para (C),
3. $$h_{CD}$$: Desnível de (C) para (D),
4. $$h_{DA}$$: Desnível de (D) para (A).

A soma dos desníveis em um circuito fechado deve ser zero:

$$
h_{AB} + h_{BC} + h_{CD} + h_{DA} = 0
$$

Devido a erros nas medições, esta condição pode não ser satisfeita, e as observações precisam ser ajustadas.

***

### Dados Observados

| Observação | Valor Observado ((m)) | Precisão ((mm)) |
| ---------- | --------------------- | --------------- |
| $$h_{AB}$$ | (1.23)                | (1.0)           |
| $$h_{BC}$$ | (2.34)                | (0.8)           |
| $$h_{CD}$$ | (-1.56)               | (0.6)           |
| $$h_{DA}$$ | (-2.05)               | (0.9)           |

***

### Montagem do Sistema

#### 1. Matriz de Condição B

A matriz representa a relação funcional entre as observações. Neste caso:

$$
\mathbf{B} = \begin{bmatrix}
1 & 1 & 1 & 1
\end{bmatrix}
$$

#### 2. Vetor de Observações Y

Os valores observados dos desníveis:

$$
\mathbf{y} = \begin{bmatrix}
1.23 \\
2.34 \\
-1.56 \\
-2.05
\end{bmatrix}
$$

#### 3. Vetor de Condições b

O valor esperado para o fechamento do circuito:

$$
\mathbf{b} = 0
$$

#### 4. Matriz de Covariância \$$\mathbf{Q}\_e \$$

Diagonal contendo as variâncias das observações:

$$
\mathbf{Q}_e = \text{diag}(1.0^2, 0.8^2, 0.6^2, 0.9^2) = 
\begin{bmatrix}
1.00 & 0    & 0    & 0    \\
0    & 0.64 & 0    & 0    \\
0    & 0    & 0.36 & 0    \\
0    & 0    & 0    & 0.81
\end{bmatrix}
$$

***

### Ajuste pelo Método Correlato

O ajuste minimiza os resíduos ((\mathbf{e})) para satisfazer:

#### Minimizar:

$$
\mathbf{e}^T \mathbf{Q}_e^{-1} \mathbf{e}
$$

#### Sujeito a:

$$
\mathbf{B} (\mathbf{y} + \mathbf{e}) = \mathbf{b}
$$

O sistema linear a ser resolvido é:

$$
\begin{bmatrix}
\mathbf{Q}_e^{-1} & \mathbf{B}^T \\
\mathbf{B} & \mathbf{0}
\end{bmatrix}
\begin{bmatrix}
\mathbf{e} \\
\boldsymbol{\lambda}
\end{bmatrix}
=
\begin{bmatrix}
-\mathbf{Q}_e^{-1} \mathbf{y} \\
\mathbf{b} - \mathbf{B} \mathbf{y}
\end{bmatrix}
$$

***

### Resultados Ajustados

| Observação | Valor Ajustado ((m)) | Correção ((e\_i)) |
| ---------- | -------------------- | ----------------- |
| (h\_{AB})  | (1.22)               | (-0.01)           |
| (h\_{BC})  | (2.32)               | (-0.02)           |
| (h\_{CD})  | (-1.58)              | (-0.02)           |
| (h\_{DA})  | (-2.04)              | (+0.01)           |

A soma dos desníveis ajustados é:

$$
1.22 + 2.32 - 1.58 - 2.04 = 0
$$

***

### Conclusões

* O Método Correlato ajustou os desníveis observados para satisfazer a condição de fechamento do circuito.
* As correções $$e_i$$foram pequenas, indicando que as observações eram confiáveis.
* A matriz de covariância $$(\mathbf{Q}_e)$$ garantiu maior peso para observações mais precisas.

Este exemplo demonstra a eficiência do Método Correlato no ajuste e validação de redes de nivelamento.




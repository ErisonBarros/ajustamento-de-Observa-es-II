# Método Correlato

## Explicação do Método Correlato

O **Método Correlato**, também conhecido como **Método das Equações de Condição**, é amplamente utilizado em Geodésia para ajustar observações, especialmente em redes geodésicas. Ele considera as relações ou vínculos funcionais entre as observações, ao invés de trabalhar diretamente com elas de forma isolada.

***

### 1. Conceito Fundamental

No Método Correlato, as observações são relacionadas por **condições que devem ser satisfeitas**. Essas condições são expressas como equações representando restrições geométricas ou físicas.

#### Exemplo de Condição

Em um triângulo, a soma dos ângulos internos deve ser igual a ( \pi ) radianos (ou (180^\circ)):

$$
\alpha + \beta + \gamma - \pi = 0
$$

Onde:

* $$\alpha, \beta, \gamma$$: Ângulos observados.
* $$-\pi$$: Vínculo geométrico.

***

### 2. Representação Matemática

A equação geral do Método Correlato é dada por:

$$
\mathbf{B} \mathbf{y} = \mathbf{b}
$$

Onde:

* (\mathbf{B}): Matriz dos coeficientes das condições ((p \times m)).
* (\mathbf{y}): Vetor de observações ((m \times 1)).
* (\mathbf{b}): Vetor de constantes ((p \times 1)).

***

### 3. Princípio de Ajustamento

O Método Correlato minimiza os resíduos ajustados $$\mathbf{e}$$, garantindo que as condições sejam satisfeitas. O problema de minimização pode ser descrito como:

#### Minimizar:

$$
\mathbf{e}^T \mathbf{Q}_e^{-1} \mathbf{e}
$$

#### Sujeito a:

$$
\mathbf{B} (\mathbf{y} + \mathbf{e}) = \mathbf{b}
$$

***

### 4. Solução Matemática

A solução utiliza **multiplicadores de Lagrange** para incorporar as condições no problema de minimização. O sistema resultante é:

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

Onde:

* (\mathbf{Q}\_e): Matriz de variâncias e covariâncias das observações.
* (\boldsymbol{\lambda}): Multiplicadores de Lagrange.

A solução fornece:

* (\mathbf{e}): Correções nas observações.
* (\boldsymbol{\lambda}): Multiplicadores associados às condições.

***

### 5. Aplicações do Método Correlato

1. **Ajuste de redes geodésicas**:
   * Estimativa de coordenadas com vínculos geométricos.
2. **Controle de qualidade**:
   * Identificação de erros sistemáticos nas observações.
3. **Modelagem geométrica**:
   * Representação de superfícies ou volumes com restrições específicas.

***

### 6. Vantagens do Método Correlato

* **Clareza nas condições**: Torna explícitas as relações geométricas ou físicas entre as observações.
* **Flexibilidade**: Adapta-se a diferentes situações com condições específicas.
* **Identificação de inconsistências**: Detecta discrepâncias nos dados.

***

### 7. Exemplo Prático

#### Problema

Considere uma rede de nivelamento onde a soma dos desníveis em um circuito fechado deve ser igual a zero:

$$
h_1 + h_2 + h_3 + h_4 = 0
$$

Neste caso:

* $$\mathbf{B}$$ = \[1 , 1 , 1 , 1],
* $$\mathbf{y}$$ = $$[h_1, h_2, h_3, h_4]^T$$,
* $$\mathbf{b} = 0$$.

O Método Correlato ajusta os desníveis observados ((h\_i)) para que satisfaçam a condição acima.

***

O **Método Correlato** é uma ferramenta poderosa para ajustar dados geodésicos, validar condições geométricas e impor vínculos em sistemas complexos.

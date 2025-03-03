# Método Correlato

## Explicação do Método Correlato

O **Método Correlato**, também conhecido como **Método das Equações de Condição**, é amplamente utilizado em Geodésia para ajustar observações, especialmente em redes geodésicas. Ele considera as relações ou vínculos funcionais entre as observações, ao invés de trabalhar diretamente com elas de forma isolada.

## Equação de Condição no Método dos Correlatos

O **Método dos Correlatos** é uma abordagem matemática utilizada no ajustamento de observações geodésicas. Ele considera as relações entre as observações ajustadas, garantindo que satisfaçam determinadas condições impostas pelo modelo.

### 1. Definição Geral

A equação fundamental do Método dos Correlatos é representada por:

$$
F(L_a) = 0
$$

Onde:

* $$L_a$$ é o vetor das **observações ajustadas** $$( n \times 1 )$$.
* $$F$$é uma **função linear ou não linear** que relaciona os parâmetros com as observações ajustadas.

***

### 2. Representação Matricial

A forma matricial do sistema de equações de observação é dada por:

$$
\mathbf{B} \mathbf{V} + \mathbf{W} = 0
$$

Onde:

* $$\mathbf{B}$$$$( r \times n )$$ é a **matriz dos coeficientes** ou matriz das **derivadas parciais** (caso de funções não lineares).
* $$\mathbf{V}$$ $$( n \times 1 )$$ é o **vetor dos resíduos** (diferença entre observações ajustadas e observações brutas).
* $$\mathbf{W}$$$$( r \times 1 )$$ é o **vetor do erro de fechamento**, indicando a inconsistência das observações antes do ajustamento.

***

### 3. Ajustamento das Observações

O ajuste das observações no Método dos Correlatos segue o princípio da minimização dos resíduos sujeitos às equações de condição:

#### **Minimizar:**

$$
\mathbf{V}^T \mathbf{Q}^{-1} \mathbf{V}
$$

#### **Sujeito a:**

$$
\mathbf{B} \mathbf{V} + \mathbf{W} = 0
$$

Onde ( \mathbf{Q} ) é a matriz de variâncias e covariâncias das observações.

A solução é obtida resolvendo o seguinte sistema aumentado:

$$
\begin{bmatrix}
\mathbf{Q}^{-1} & \mathbf{B}^T \\
\mathbf{B} & \mathbf{0}
\end{bmatrix}
\begin{bmatrix}
\mathbf{V} \\
\boldsymbol{\lambda}
\end{bmatrix}
=
\begin{bmatrix}
-\mathbf{Q}^{-1} \mathbf{L} \\
-\mathbf{W}
\end{bmatrix}
$$

Onde $$\boldsymbol{\lambda}$$ são os multiplicadores de Lagrange associados às equações de condição.

***

### 4. Aplicação em Redes Geodésicas

Em um **circuito de nivelamento fechado**, as equações de condição garantem que a soma dos desníveis ao longo do percurso seja zero:

$$
h_1 + h_2 + h_3 + h_4 = 0
$$

Isso pode ser representado na forma matricial:

$$
\mathbf{B} =
\begin{bmatrix}
1 & 1 & 1 & 1
\end{bmatrix}
$$

$$
\mathbf{y} =
\begin{bmatrix}
h_1 \\
h_2 \\
h_3 \\
h_4
\end{bmatrix}
$$

$$
\mathbf{b} = 0
$$

Se houver inconsistência nos desníveis observados, o Método dos Correlatos ajusta as observações para que satisfaçam a equação de fechamento.

***

### 5. Conclusão

As **equações de condição** são fundamentais no **Método dos Correlatos** para garantir a consistência das observações geodésicas. Esse método ajusta as observações respeitando restrições geométricas e físicas, garantindo maior precisão e confiabilidade nos resultados.

***

### 1. Conceito Fundamental

No Método Correlato, as observações são relacionadas por **condições que devem ser satisfeitas**. Essas condições são expressas como equações representando restrições geométricas ou físicas.

#### Exemplo de Condição

Em um triângulo, a soma dos ângulos internos deve ser igual a $$\pi$$ radianos $$ou (180^\circ)$$:

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

* $$\mathbf{B}$$: Matriz dos coeficientes das condições $$(p \times m)$$.
* $$\mathbf{y}$$: Vetor de observações $$(m \times 1)$$
* $$\mathbf{b}$$: Vetor de constantes $$(p \times 1)$$

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

* $$\mathbf{Q}_e$$ Matriz de variâncias e covariâncias das observações.
* $$\boldsymbol{\lambda}$$: Multiplicadores de Lagrange.

A solução fornece:

* $$\mathbf{e}$$: Correções nas observações.
* $$\boldsymbol{\lambda}$$: Multiplicadores associados às condições.

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

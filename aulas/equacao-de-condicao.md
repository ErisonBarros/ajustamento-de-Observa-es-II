# Equação de Condição

## Equação de Condição

### Introdução

As **equações de condição** são amplamente utilizadas na Geodésia e no Ajustamento de Observações. Elas representam vínculos matemáticos entre as observações, garantindo que certas restrições sejam respeitadas. Essas equações são fundamentais para o **Método das Equações de Condição**, também conhecido como **Método Correlato**.

***

### Definição Matemática

Dado um conjunto de ( m ) observações representado pelo vetor:

$$
\mathbf{y} =
\begin{bmatrix}
y_1 \\
y_2 \\
\vdots \\
y_m
\end{bmatrix}
$$

As equações de condição impõem restrições na forma de ( p ) equações lineares independentes:

$$
\mathbf{B} \mathbf{y} = \mathbf{b}
$$

Onde:

* $$\mathbf{B}$$ é uma matriz de coeficientes das equações de condição $$( p \times m )$$.
* $$\mathbf{y}$$é o vetor das observações $$( m \times 1 )$$.
* $$\mathbf{b}$$ é o vetor das constantes $$( p \times 1 )$$.

Se a matriz ( \mathbf{B} ) for completa, significa que todas as condições foram corretamente especificadas.

***

### Aplicação Prática: Rede de Nivelamento

Um exemplo clássico do uso das equações de condição ocorre em um **circuito fechado de nivelamento**. Para garantir a consistência dos desníveis medidos entre pontos sucessivos, a soma dos desníveis deve ser zero:

$$
h_1 + h_2 + h_3 + h_4 = 0
$$

Neste caso:

*   A matriz ( \mathbf{B} ) é:

    $$
    \mathbf{B} =
    \begin{bmatrix}
    1 & 1 & 1 & 1
    \end{bmatrix}
    $$
*   O vetor de observações ( \mathbf{y} ) contém os desníveis medidos:

    $$
    \mathbf{y} =
    \begin{bmatrix}
    h_1 \\
    h_2 \\
    h_3 \\
    h_4
    \end{bmatrix}
    $$
*   O vetor de condição ( \mathbf{b} ) é:

    $$
    \mathbf{b} = 0
    $$

Caso a soma dos desníveis observados não seja exatamente zero devido a erros de medição, o Método Correlato é utilizado para ajustar os valores e satisfazer a equação de condição.

***

### Ajuste pelo Método Correlato

O ajuste das observações minimiza os resíduos ( \mathbf{e} ) sujeitos à condição:

#### Minimização:

$$
\mathbf{e}^T \mathbf{Q}_e^{-1} \mathbf{e}
$$

#### Sujeito a:

$$
\mathbf{B} (\mathbf{y} + \mathbf{e}) = \mathbf{b}
$$

O sistema linear resultante é:

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

A solução fornece as correções ( \mathbf{e} ) que devem ser aplicadas às observações $$\mathbf{y}$$ para satisfazer as equações de condição.

***

### Observação:

As equações de condição são essenciais para garantir a **consistência e qualidade dos dados geodésicos**. O **Método Correlato** permite ajustar observações respeitando vínculos matemáticos, reduzindo erros e assegurando resultados confiáveis.

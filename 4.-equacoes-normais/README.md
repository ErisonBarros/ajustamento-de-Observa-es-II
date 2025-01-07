# 4. EQUAÇÕES NORMAIS

## 10.2 — Equações Normais

Repetindo a marcha do capítulo precedente, além de minimizar a forma quadrática fundamental devemos proceder de maneira que os resíduos (dos valores observados) e as correções ( X ) (dos parâmetros aproximados) atendam à injunção representada pelo modelo (10.1.7). Utilizando a técnica lagrangiana definamos a função:

$$\phi = V^T P V - 2K^T (AX + BV + W) = \text{mínimo} \tag{10.2.1}$$

sendo ( K ), como anteriormente, o vetor dos multiplicadores de Lagrange ou dos correlatos.

Anulando as derivadas parciais em relação a ( V ), ( K ) e ( X ):

$$\frac{\partial \phi}{\partial V} = 2P V - 2B^T K \cdot P V - B^T K = 0, \tag{10.2.2}$$

$$\frac{\partial \phi}{\partial K} = -2(AX + BV + W) \cdot AX + BV + W = 0, \tag{10.2.3}$$

$$\frac{\partial \phi}{\partial X} = -2A^T K \cdot A^T K = 0. \tag{10.2.4}$$



***

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

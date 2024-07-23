# Elipses (intervalo) de Confiança

* Distribuição normal 2D: corte da FDP em plano paralelo ao XY = elipse de confiança
*   Elipse de erros padrão em (P(x\_0, y\_0)): Caso particular com

    $$
    \begin{bmatrix} x - x_0 \\ y - y_0 \end{bmatrix}^T \Sigma_P^{-1} \begin{bmatrix} x - x_0 \\ y - y_0 \end{bmatrix} = 1
    $$

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

*   Caso geral:

    $$
    \frac{1}{2} \begin{bmatrix} x - x_0 \\ y - y_0 \end{bmatrix}^T \Sigma_P^{-1} \begin{bmatrix} x - x_0 \\ y - y_0 \end{bmatrix} = F(2, n-u, \alpha)
    $$

Distribuição  de Probabilidade F

Logo, para obter os semi-eixos (a, b) da elipse de erros com nível de confiança $$NC = 1 - \alpha$$, basta multiplicar os semi-eixos da elipse de erros padrão pelo escalar $$c = \sqrt{2 \cdot F_{(2, n-u)}}$$.

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

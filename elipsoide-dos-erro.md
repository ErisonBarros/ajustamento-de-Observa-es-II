# Elipsoide dos Erro

### Elipsoides de Erros

#### Conversão dos seis elementos da matriz de covariância

Os seis elementos da matriz de covariância $$(\sigma_{x}^2, \sigma_{y}^2, \sigma_{z}^2, \sigma_{xy}, \sigma_{xz}, \sigma_{yz})$$ são convertidos nos seis parâmetros do elipsoide de erros $$(a, b, c, k, p, \omega)$$

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>





Solução: autovalores $$\lambda$$ e autovetores $$A_{3x1}$$ da matriz de covariância do ponto (P)

$$
\Sigma_{x,y,z} = \begin{bmatrix} \sigma_x^2 & \sigma_{x,y} & \sigma_{x,z} \\ \sigma_{y,x} & \sigma_y^2 & \sigma_{y,z} \\ \sigma_{z,x} & \sigma_{z,y} & \sigma_z^2 \end{bmatrix}
$$

$$
|\Sigma_{x,y,z} - \lambda \cdot I| = 0
$$

$$
\Lambda_a = \begin{bmatrix} a_x \\ a_y \\ a_z \end{bmatrix}, \quad \Lambda_b = \begin{bmatrix} b_x \\ b_y \\ b_z \end{bmatrix}, \quad \Lambda_c = \begin{bmatrix} c_x \\ c_y \\ c_z \end{bmatrix}
$$

$$
I = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

*   **Equação característica:**

    $$
    \begin{bmatrix} \sigma_{x}^2 - \lambda & \sigma_{xy} & \sigma_{xz} \\ \sigma_{xy} & \sigma_{y}^2 - \lambda & \sigma_{yz} \\ \sigma_{xz} & \sigma_{yz} & \sigma_{z}^2 - \lambda \end{bmatrix} \begin{bmatrix} a_{x} \\ a_{y} \\ a_{z} \end{bmatrix} = 0
    $$

$$
\Lambda_a^T \Lambda_b = \Lambda_a^T \Lambda_c = \Lambda_b^T \Lambda_c = 0
$$

*   **Autovalores (\lambda):**

    $$\lambda = \lambda_{max}, \lambda_{med}, \lambda_{min}$$

    * $$a = \sqrt{\lambda_{max}}$$
    * $$b = \sqrt{\lambda_{med}}$$
    * $$c = \sqrt{\lambda_{min}}$$

#### Visualização do Elipsoide de Erros

* A matriz de rotação (Q) e o vetor de deslocamento$$\vec{\epsilon}$$ definem a orientação e a posição do elipsoide em relação ao ponto (P).

#### Exemplo de Configuração do Elipsoide no Espaço

* O elipsoide é plotado com base nos autovetores, que definem a orientação dos eixos principais, e os autovalores determinam o comprimento dos semi-eixos.

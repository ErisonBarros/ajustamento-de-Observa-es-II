# Elipse de Erros Relativas entre Pontos

### Elipse de Erros Relativa entre Pontos

**Considere dois pontos distintos (i) e (j) em uma rede horizontal:**

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>



* **Elipse em (i) (absoluta)**
* **Elipse em (j) (absoluta)**
* **Elipse entre (i) e (j) (relativa)**

#### Diferença de Coordenadas

$$
\Delta = \begin{bmatrix} \Delta x \\ \Delta y \end{bmatrix} = \begin{bmatrix} x_j - x_i \\ y_j - y_i \end{bmatrix}
$$

#### Matriz de Covariância

$$
\Sigma_A = \begin{bmatrix} \sigma_{x_i}^2 & \sigma_{x_iy_i} & \sigma_{x_i x_j} & \sigma_{x_i y_j} \\ \sigma_{y_ix_i} & \sigma_{y_i}^2 & \sigma_{y_i x_j} & \sigma_{y_i y_j} \\ \sigma_{x_j x_i} & \sigma_{x_j y_i} & \sigma_{x_j}^2 & \sigma_{x_j y_j} \\ \sigma_{y_j x_i} & \sigma_{y_j y_i} & \sigma_{y_j x_j} & \sigma_{y_j}^2 \end{bmatrix}
$$

#### Transformação da Matriz de Covariância

$$
\Sigma_A = G(\Sigma_{x_iy_i}, \Sigma_{x_jy_j})G^T
$$

$$
G = \begin{bmatrix} -1 & 0 & 1 & 0 \\ 0 & -1 & 0 & 1 \end{bmatrix}
$$

$$
\Sigma_{\Delta} = \begin{bmatrix} \sigma_{\Delta x}^2 & \sigma_{\Delta x, \Delta y} \\ \sigma_{\Delta y, \Delta x} & \sigma_{\Delta y}^2 \end{bmatrix} = \begin{bmatrix} \sigma_{x_i}^2 + \sigma_{x_j}^2 - 2\sigma_{x_i x_j} & \sigma_{x_i y_i} + \sigma_{x_j y_j} - \sigma_{x_i y_j} - \sigma_{x_j y_i} \\ \sigma_{x_i y_i} + \sigma_{x_j y_j} - \sigma_{x_i y_j} - \sigma_{x_j y_i} & \sigma_{y_i}^2 + \sigma_{y_j}^2 - 2\sigma_{y_i y_j} \end{bmatrix}
$$

#### Cálculo de (M)

$$
M = \sqrt{4\sigma_{xy}^2 + (\sigma_x^2 - \sigma_y^2)^2}
$$

#### Semi-eixos da Elipse

$$
a = \frac{1}{2} \sqrt{(\sigma_x^2 + \sigma_y^2 + M)}
$$

$$
b = \frac{1}{2} \sqrt{(\sigma_x^2 + \sigma_y^2 - M)}
$$

#### Orientação da Elipse

$$
\theta = \frac{1}{2} \arctan2\left(\frac{2\cdot\sigma_{xy}}{\sigma_x^2 - \sigma_y^2}\right)
$$

**O ângulo 2t varia de -180° a 180°.**



#### **Ajustamento em rede:**

* Covariância entre i e j!

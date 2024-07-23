# Page

### Elipse dos Erros

A correspondente MVC pode ser obtida por propagação: Σ'\_xy' = D Σ\_xy D^T

Σ'\_xy' =

$$
\begin{bmatrix} \cos(t) & \sin(t) \\ -\sin(t) & \cos(t) \end{bmatrix} \begin{bmatrix} \sigma^2_x & \sigma_{xy} \\ \sigma_{xy} & \sigma^2_y \end{bmatrix} \begin{bmatrix} \cos(t) & -\sin(t) \\ \sin(t) & \cos(t) \end{bmatrix}
$$

Segue-se que:

$$
\sigma_{x'}^2 = \sigma_x^2 \cos^2(t) + \sigma_y^2 \sin^2(t) + 2\sigma_{xy}\sin(t)\cos(t)
$$

$$
\sigma_{y'}^2 = \sigma_x^2 \sin^2(t) + \sigma_y^2 \cos^2(t) - 2\sigma_{xy}\sin(t)\cos(t)
$$

$$
\sigma_{x'y'} = -(\sigma_x^2 - \sigma_y^2)\sin(t)\cos(t) + \sigma_{xy}(\cos^2(t) - \sin^2(t))
$$

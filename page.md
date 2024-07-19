# Page

### Elipse dos Erros

A correspondente MVC pode ser obtida por propagação: Σ'\_xy' = D Σ\_xy D^T

Σ'\_xy' =

$$
\begin{bmatrix} \cos(t) & \sin(t) \\ -\sin(t) & \cos(t) \end{bmatrix} \begin{bmatrix} \sigma^2_x & \sigma_{xy} \\ \sigma_{xy} & \sigma^2_y \end{bmatrix} \begin{bmatrix} \cos(t) & -\sin(t) \\ \sin(t) & \cos(t) \end{bmatrix}
$$

Segue-se que:

$$sigma'^2_x = \sigma^2_x \cos^2(t) + \sigma^2_y \sin^2(t) + 2\sigma_{xy} \sin(t)\cos(t)$$

$$sigma'^2_y = \sigma^2_x \sin^2(t) + \sigma^2_y \cos^2(t) - 2\sigma_{xy} \sin(t)\cos(t)$$

$$sigma'{xy} = (\sigma^2_x - \sigma^2_y) \sin(t)\cos(t) + \sigma{xy} (\cos^2(t) - \sin^2(t))$$

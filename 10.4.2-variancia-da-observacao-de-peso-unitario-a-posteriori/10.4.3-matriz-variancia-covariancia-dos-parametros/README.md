# 10.4.3 — Matriz Variância-Covariância dos Parâmetros

####

Para obter uma expressão para a matriz variância-covariância dos parâmetros ajustados vamos aplicar a "lei de propagação" à (10.3.16) na qual consideramos constantes todas as matrizes do 2º membro, à exceção de ( W ):

$$X = ZW \tag{10.4.8}$$

com

$$Z = -(A^T M^{-1} A)^{-1} A^T M^{-1}, \tag{10.4.9}$$

$$W = F(L_b, X_0). \tag{10.4.10}$$

Primeiramente apliquemos a lei de propagação à (10.4.10):

$$\Sigma_w = \frac{dW}{dL_b} \Sigma_{L_b} \left( \frac{dW}{dL_b} \right)^T = B \Sigma_{L_b} B^T,$$

$$\Sigma_w = \sigma_0^2 BP^{-1} B^T = \sigma_0^2 M, \tag{10.4.11}$$

# Ajustamento de Observações

**1. Método dos Mínimos Quadrados (MMQ)**

* **Objetivo**: Minimizar a soma dos quadrados dos resíduos.
* **Características**:
  * Estimativas imparciais e de variância mínima.
  * Aplicável a diversos problemas, como redes de nivelamento e poligonais.
* **Equações**:
  * $$𝑉=𝐴𝑋−𝐿V=AX−L$$
  * $$𝑁=𝐴𝑇𝑃𝐴N=ATPA$$
  * $$𝑋=(𝐴𝑇𝑃𝐴)−1𝐴𝑇𝑃𝐿X=(ATPA)−1ATPL$$
* **Passos**:
  1. Formular equações de observação.
  2. Construir matriz de coeficientes $$𝐴A$$ e vetor de observações $$𝐿L$$.
  3. Calcular matriz normal $$𝑁N$$ e vetor de correções $$𝑋X$$.
  4. Ajustar observações e calcular resíduos $$𝑉V$$.

**2. Método das Equações de Condição (Correlatos)**

* **Objetivo**: Ajustar observações que devem satisfazer condições matemáticas.
* **Características**:
  * Utilizado para observações que precisam atender relações matemáticas.
  * Minimiza os erros de fechamento nas equações de condição.
* **Equações**:
  * $$𝐹(𝐿𝑎)=0F(La)=0$$
  * $$𝐿𝑎=𝐿𝑏+𝑉La=Lb+V$$
  * $$𝑊=𝐹(𝐿𝑏)W=F(Lb)$$
  * $$𝑊+𝐵⋅𝑉=0W+B⋅V=0$$
* **Passos**:
  1. Escrever equações de condição.
  2. Calcular vetor de erro de fechamento $$𝑊W$$.
  3. Determinar matriz $$𝐵B$$.
  4. Definir matriz dos pesos (inverso da variância).
  5. Resolver sistema linearizado.
  6. Conferir vetor $$𝑊W$$ ajustado.
  7. Calcular variância a posteriori.
  8. Calcular matriz variância-covariância.
  9. Calcular altitudes ajustadas.
  10. Determinar precisão das altitudes ajustadas.

**3. Método Paramétrico**

* **Objetivo**: Ajustar parâmetros de um modelo matemático.
* **Características**:
  * Utilizado quando as observações são funções de parâmetros desconhecidos.
  * Estimativas que melhor se ajustam aos dados observacionais.
* **Equações**:
  * $$𝑌=𝑓(𝑋)+𝜖Y=f(X)+ϵ$$
* **Passos**:
  1. Definir modelo matemático.
  2. Coletar dados observacionais.
  3. Ajustar parâmetros do modelo.
  4. Validar o modelo ajustado.

#### Conclusão

Os métodos de ajustamento garantem precisão e confiabilidade dos dados em topografia e geodésia, permitindo a minimização dos erros e obtenção de resultados precisos e confiáveis.

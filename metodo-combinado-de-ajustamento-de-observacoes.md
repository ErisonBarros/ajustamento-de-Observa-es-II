# Método Combinado de Ajustamento de Observações

### Introdução

O método combinado de ajustamento de observações é uma técnica avançada utilizada em geomática e outras áreas para ajustar valores observados e parâmetros simultaneamente. Este método é mais genérico que os métodos paramétrico e dos correlatos, pois combina elementos de ambos. A seguir, apresentaremos os principais conceitos, equações e procedimentos para a aplicação do método combinado.

### Conceitos Básicos

* **Valores observados (L):** Medidas feitas diretamente.
* **Parâmetros (X):** Variáveis ajustadas indiretamente através das observações.
* **Função de ajuste (F):** Relação matemática que descreve o sistema de observações e parâmetros.

### Equações Fundamentais

O modelo matemático do método combinado é expresso pela função:

$$F(X, L) = 0$$

Para linearizar esta função, fazemos:

$$F(X + \Delta X, L + \Delta L) \approx F(X, L) + A \Delta X + B \Delta L$$

Onde ( A ) e ( B ) são as matrizes de derivadas parciais de ( F ) com respeito a ( X ) e ( L ), respectivamente.

### Passos para o Ajustamento

1.  **Definir as Observações e Parâmetros Iniciais:**

    ```markdown
    Lb = [observações iniciais]
    X0 = [parâmetros iniciais]
    P = [matriz de pesos]
    ```
2. **Cálculo das Matrizes A e B:**

$$
A = \frac{∂F}{∂X}|_{(X0, Lb)}
$$

$$
B = \frac{∂F}{∂X} |_{(X0, Lb)}
$$

1.  **Formação do Sistema Linearizado:**

    ```markdown
    AX + BV + W = 0
    ```

    Onde ( W ) é o vetor dos resíduos iniciais.
2. **Resolução das Equações Normais:**

#### 4. Resolução das Equações Normais

Para resolver o sistema linearizado, seguimos os seguintes passos:

1.  **Multiplicação pela Transposta:** Multiplicamos a equação linearizada $$AX + BV + W = 0$$ pela transposta de ( A ) e de ( B ) para formar o sistema das equações normais:

    $$A^T P (AX + BV + W) = 0$$$$B^T P (AX + BV + W) = 0$$

    Isso resulta no sistema de equações:

    $$A^T P A X + A^T P B V + A^T P W = 0$$ $$B^T P A X + B^T P B V + B^T P W = 0$$
2.  **Formação das Matrizes ( K ) e ( C ):** Reorganizamos as equações normais na forma matricial:

    $$K = \begin{bmatrix} A^T P A & A^T P B \ B^T P A & B^T P B \end{bmatrix}$$

    $$C = -\begin{bmatrix} A^T P W \ B^T P W \end{bmatrix}$$
3. **Resolução do Sistema Linear:** Calculamos $$\Delta X$$ e $$\Delta V$$resolvendo o sistema:

&#x20;          $$K.\frac{\Delta X} {\Delta Y} =C$$

Para isso, podemos usar métodos numéricos, como a decomposição LU ou a inversão direta da matriz $$K$$.

**Implementação em Python**

Aqui está como você pode implementar a resolução desse sistema em Python:

```markdown
TBBPM = B^T P B
WMAAMAX = (A^T P A)^{-1} (A^T P W - B^T P V)
X = X0 + ΔX
```

1. **Iterações:** Repetir os cálculos acima até que a correção ( ΔX ) seja suficientemente pequena.

### Exemplo Prático

Considere o ajuste das coordenadas de quatro pontos observados:

* Observações: Coordenadas de quatro pontos (x, y)
* Parâmetros: Coordenadas do centro ajustado (x\_a, y\_a) e o raio ajustado (r\_a)

#### Modelo Matemático:

$$(x_i - x_a)^2 + (y_i - y_a)^2 - r_a^2 = 0$$

#### Procedimento:

1.  Definir as observações e parâmetros iniciais:

    ```markdown
    Lb = [140, 0.5, 60, 0.5, 165, 1.0, 100, 1.0, 165, 0.5, 150, 0.5, 140, 1.0, 180, 1.0]
    X0 = [70, 120, 100]
    P = eye(8)  # Matriz identidade de 8x8
    ```
2. Calcular as matrizes A e B:

$$A = ∂F/∂X |_(X0, Lb)$$

$$B = ∂F/∂L |_(X0, Lb)$$

1. Formar e resolver o sistema linearizado:

AX + BV + W = 0

$$K = \begin{bmatrix} A^T P A & A^T P B \ B^T P A & B^T P B \end{bmatrix}$$

$$C = -\begin{bmatrix} A^T P W \ B^T P W \end{bmatrix}$$



```markdown
AX + BV + W = 0
TBBPM = B^T P B
WMAAMAX = (A^T P A)^{-1} (A^T P W - B^T P V)
X = X0 + ΔX
```

1. Iterar até convergência.

### Conclusão

O método combinado de ajustamento é uma ferramenta poderosa para a correção simultânea de observações e parâmetros em sistemas de medição complexos. Através da linearização e iteração, obtemos soluções ajustadas que minimizam os erros de fechamento e proporcionam estimativas precisas dos parâmetros.

***

### Código de Exemplo em Python (Google Colab)

```python
import numpy as np

# Observações iniciais
Lb = np.array([140, 0.5, 60, 0.5, 165, 1.0, 100, 1.0, 165, 0.5, 150, 0.5, 140, 1.0, 180, 1.0])
# Parâmetros iniciais
X0 = np.array([70, 120, 100])
# Matriz de pesos (identidade)
P = np.eye(8)

# Função que define as matrizes A e B
def calcular_matrizes(X, L):
    # Implementar o cálculo das derivadas parciais
    A = np.zeros((8, 3))  # Exemplo de inicialização
    B = np.zeros((8, 8))  # Exemplo de inicialização
    # Preencher A e B com os valores corretos
    return A, B

# Iteração do ajuste
for _ in range(10):  # Exemplo de 10 iterações
    A, B = calcular_matrizes(X0, Lb)
    W = np.zeros(8)  # Vetor de resíduos
    # Formar e resolver o sistema linearizado
    TBBPM = B.T @ P @ B
    WMAAMAX = np.linalg.inv(A.T @ P @ A) @ (A.T @ P @ W - B.T @ P @ V)
    ΔX = WMAAMAX
    X = X0 + ΔX
    X0 = X  # Atualizar X0 para a próxima iteração

# Parâmetros ajustados finais
print("Parâmetros ajustados:", X)
```

# Método das Equações de Condição ou dos Correlatos

### Aula 01

#### Introdução

O método de ajustamento das equações de condição, também conhecido como método dos correlatos, visa ajustar observações ligadas a uma equação de condição, resultando em observações ajustadas. Esse método é aplicado quando se tem _r_ equações de condição e _n_ observações.

**Conceitos Fundamentais**

**Equações de condição** são relações matemáticas conhecidas que devem ser satisfeitas pelas observações, como:

* Soma dos ângulos internos de um triângulo plano = 180º
* Soma das projeções em uma poligonal fechada = 0
* Soma das diferenças de nível em um circuito de nivelamento = 0

**Diferença do método paramétrico:** No método das equações de condição, não há parâmetros, apenas observações diretas condicionadas a uma equação de condição.

#### Modelo Matemático

As observações condicionadas são modeladas pela seguinte equação:

```
F(La) = 0
```

Onde:

* **La:** Observações ajustadas
* **F:** Função que representa a equação de condição

Devido aos erros inevitáveis nas observações, as equações de condição apresentam um "erro de fechamento", **W**, que deve ser eliminado pelo método dos mínimos quadrados.

Para linearizar a função, utiliza-se a Série de Taylor:

```
F(La) = F(Lb) + V = F(Lb) + ∂F/∂Lb * (La - Lb) = 0
```

Onde:

* **Lb:** Observações originais
* **V:** Correções às observações originais
* **∂F/∂Lb:** Matriz das derivadas parciais da função F em relação às observações originais (Matriz B)

#### Modelo Linearizado

```
F(La) = F(Lb) + V = W + B * V = 0
```

Onde:

* **W:** Vetor dos erros de fechamento (F(Lb))
* **B:** Matriz das derivadas parciais (∂F/∂Lb)

#### Exemplo: Rede de Nivelamento

**Dados:**

* Rede de nivelamento com 9 observações (L1 a L9)
* 4 equações de condição
* Erros de fechamento (W) calculados

**Matriz B:** Derivadas das equações de condição em relação às observações.

**Matriz de Pesos:** Inversa da variância das observações.

#### Passos para o Método das Equações de Condição

1. **Escrever as equações de condição.**
2. **Calcular o vetor W (erros de fechamento).**
3. **Determinar a matriz B (derivadas das equações de condição).**
4. **Definir a matriz de pesos (inversa da variância).**
5. **Calcular as correções (V) e as observações ajustadas (La).**
6. **Conferir o vetor W com as observações ajustadas La.**
7. **Calcular a variância á posteriori (σ^2).**
8. **Calcular a matriz de variância-covariância das observações ajustadas (MVCLaC).**
9. **Calcular as altitudes ajustadas dos pontos.**
10. **Determinar a precisão das altitudes ajustadas (MVC\_ALT).**

#### Conclusões

O método das equações de condição é uma técnica poderosa para ajustar observações condicionadas por relações matemáticas conhecidas. Ele permite obter observações ajustadas e calcular a precisão dos resultados, levando em consideração os erros inevitáveis nas medições.

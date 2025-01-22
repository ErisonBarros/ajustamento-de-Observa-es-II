# Aula: Ajustamento com Injunções

### Introdução

O ajustamento com injunções é uma técnica utilizada em geodésia e topografia para impor restrições adicionais em um sistema de observações. Essas restrições, ou injunções, são condições que os parâmetros devem satisfazer para garantir a precisão e consistência do ajustamento.

### Equações de Condição e Injunções

Equações de condição são usadas para definir restrições entre observações, enquanto as injunções são restrições impostas diretamente aos parâmetros.

* **Equações de injunção**: ( $$C \cdot X = W$$ )
* **Modelo matemático linearizado**: $$\epsilon_{C }= W'$$

### Ajustamento Paramétrico com Injunções

O modelo matemático para injunções ponderadas é dado por: $$[ \phi(X) = \frac{1}{2} (V^T P V + (AX - L)^T Q (AX - L) + (CX - W)^T R (CX - W)) ]$$

Onde:

* ( V ) é o vetor de resíduos.
* ( P ), ( Q ) e ( R ) são as matrizes de pesos.
* ( A ) é a matriz de coeficientes das observações.
* ( C ) é a matriz de coeficientes das injunções.
* ( L ) é o vetor de observações.
* ( W ) é o vetor de injunções.

### Resolvendo o Ajustamento

Para resolver o ajustamento com injunções, derivamos a função objetivo e igualamos a zero:$$[ \frac{\partial \phi}{\partial X} = 0 ]$$

Resultando na seguinte equação matricial:$$[ (A^T P A + C^T R C) X = A^T P L + C^T R W ]$$

### Exemplos de Injunções

Alguns tipos comuns de injunções são:

* **Posição**: Fixar a coordenada de um ponto.
* **Distância**: Restringir a distância entre dois pontos.
* **Altura**: Fixar a altura de um ponto.
* **Direção**: Fixar a direção entre dois pontos.
* **Posição relativa**: Fixar a posição de um ponto relativo a outro.

### Exercício Prático

#### Exemplo de Ajustamento Paramétrico com Injunções

Dado um polígono ABCD com coordenadas conhecidas e isentas de erro no referencial $$( X_1 X_2 )$$, aplicou-se a transformação:$$[ x_1 = a + bx - dy ] [ x_2 = c + bx + dy ]$$

Após a transformação, o ponto D deve ter a coordenada fixada em (-16,00; 60,00). Os demais pontos tiveram suas coordenadas observadas conforme a tabela abaixo:

| Ponto | ( X\_1 ) | ( X\_2 ) | ( Y\_1 ) | ( Y\_2 ) |
| ----- | -------- | -------- | -------- | -------- |
| A     | 0        | 0        | 11,30    | 9,30     |
| B     | 10       | 0        | 34,70    | 84,50    |
| C     | 15       | 3        | 23,00    | 133,60   |
| D     | 5        | 5        | -16,00   | 60,00    |

**Modelo Matemático**

$$[\begin{cases} y_1 = a + bx - dy \ y_2 = c + bx + dy \end{cases} ]$$

**Passos para o Ajustamento**

1. **Modelo Funcional**: Define as relações matemáticas entre as observações e os parâmetros.
2. **Equações de Injunção**: Impõem restrições adicionais aos parâmetros.
3. **Matriz de Pesos**: Define a precisão relativa das observações.
4. **Cálculo das Matrizes**:
   * ( A ): Matriz de coeficientes das observações.
   * ( C ): Matriz de coeficientes das injunções.
   * ( P ): Matriz de pesos das observações.
   * ( R ): Matriz de pesos das injunções.
5. **Solução do Sistema**: Resolve o sistema de equações lineares para encontrar os valores ajustados dos parâmetros.

### Conclusão

O ajustamento com injunções é uma técnica poderosa para melhorar a precisão e consistência dos resultados em geodésia e topografia. Ao impor restrições adicionais, é possível obter um modelo mais robusto e confiável.

***

### Referências

Machado, A. M. L. (2017). Ajustamento de Observações – GA751. Universidade Federal do Paraná, Setor de Ciências da Terra, Departamento de Geomática.

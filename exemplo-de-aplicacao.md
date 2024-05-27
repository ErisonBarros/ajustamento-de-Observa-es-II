# Exemplo de Aplicação

Calcular com o método das equações de condição dos correlatos a rede de nivelamento do livro de Camil Gemael.

[![Imagem4](https://i.ibb.co/dbRCs8V/Imagem4.jpg)](https://imgbb.com/)

| Linha | Δh (m)  | Distância (km) |
| ----- | ------- | -------------- |
| 1     | 10038   | 114            |
| 2     | 8297    | 284            |
| 3     | 1949    | 321            |
| 4     | 5217    | 603            |
| 5     | 10244   | 675            |
| 6     | 1562    | 084            |
| 7     | 4837    | 294            |
| 8     | 3370    | 201            |
| 9     | 15979   | 528            |
| RNA   | 33831 m |                |
| RNB   | 19316 m |                |
| RNC   | 2791 m  |                |

É possível formar 4 Equações de Condição: $$𝐹(𝐿𝑎)=0F(La)=0$$.

**Passo a Passo do Método das Equações de Condição**

1. **Escrever as equações de condição:** $$𝐹(𝐿𝑎)=0F(La)=0$$ $$𝑅𝑁𝑐+𝐿1𝑎+𝐿2𝑎+𝐿6𝑎−𝐿8𝑎−𝑅𝑁𝑏=0RNc+L1a+L2a+L6a−L8a−RNb=0$$ $$𝑅𝑁𝑎−𝐿9𝑎+𝐿7𝑎−𝐿8𝑎−𝑅𝑁𝑏=0RNa−L9a+L7a−L8a−RNb=0$$ $$𝐿2𝑎+𝐿3𝑎−𝐿5𝑎=0L2a+L3a−L5a=0$$ $$𝐿3𝑎−𝐿4𝑎+𝐿7𝑎−𝐿6𝑎=0L3a−L4a+L7a−L6a=0$$
2. **Calcular o vetor** $$𝑊W$$ **("erro de fechamento"):** Determinar a matriz $$𝐵B$$ - Matriz das derivadas das Equações de Condição com relação a todas as observações.
3. **Determinar a matriz dos Pesos (o inverso da variância):** $$𝑀𝑉𝐶𝐿𝑎𝐶=Σ𝐶×(inv(𝑃)−inv(𝑃)×𝐵′×inv(𝐵×inv(𝑃)×𝐵′)×𝐵×inv(𝑃))MVCLaC=ΣC×(inv(P)−inv(P)×B′×inv(B×inv(P)×B′)×B×inv(P))$$ Atenção à Variância á Posteriori.
4. **Cálculos:** Conferir com o vetor $$𝑊W$$ agora com as observações ajustadas $$𝐿𝑎La$$. $$𝐹(𝐿𝑎)=0F(La)=0$$
5. **Calcular a Variância á Posteriori:** Os graus de liberdade são iguais ao número de equações de condição, no exemplo são quatro. Variância a posteriori = 0.2964.
6. **Calcular a matriz variância-covariância das observações ajustadas (correlatos):**
7. **Calcular as Altitudes Ajustadas dos cinco pontos:** Utilizando qualquer caminho, as altitudes são calculadas a partir dos RRNN considerando as Observações Ajustadas.
8. **Determinar a precisão das altitudes ajustadas (parâmetros):** A Matriz Variância /Covariânca das altitudes ajustadas e os respectivos desvios. $$𝑀𝑉𝐶_𝐴𝐿𝑇=𝐺×𝑀𝑉𝐶𝐿𝑎×𝐺′MVC_ALT=G×MVCLa×G′$$
9. **Lei da propagação das variâncias:** Onde $$𝐺G$$ é a matriz dos coeficientes das Observações ajustadas.

**Conclusão**

O método das Equações de Condição é uma técnica rigorosa que permite o ajustamento das observações para atender a condições específicas, eliminando erros de fechamento através do método dos mínimos quadrados, garantindo precisão nos resultados ajustados.

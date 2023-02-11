# A - Álgebra Booleana e Implementação de Funções Lógicas com CIs

| Data da entrega| 
|----------------|
| Quarta - 01/03 |

Nesse projeto iremos utilizar a álgebra booleana para obter as funções lógicas de um sistema as quais deverão ser implementadas utilizando CIs.

Esse projeto deverá ser realizado em trios e os arquivos devem ser enviados pelo Forms.

Queremos controlar o robô da figura a seguir:

![](carro.png){width=400}


onde y1 e y2 são sinais de saída (de 2 bits cada) para os motores que controlam as esteiras da esquerda e direita. x1, x2, x3 e x4 são sensores (bumpers) para detectar a colisão do robô.

Os sinais de y1 e y2 (de 2 bits cada) descrevem os seguintes movimentos:

- "10" - motor ligado diretamente (andando para frente)
- "01" - motor ligado reversamente (andando para trás) 
- "00" - motor desligado

> os sinais y1 e y2 devem ser ligados as entradas I1, I2, I3 e I4 da ponte H.

O controle deve ser feito da seguinte forma:

1. Todos os motores devem ser desligados se (x1 ou x2) indicar colisão juntamente com (x3 ou x4).
2. Todos os motores devem ser ligados diretamente se nenhum sensor indicar colisão.
3. Ambos os motores devem ser ligados reversamente se os sensores x1 e x2 detectarem colisão.
4. Ambos os motores devem ser ligados diretamente se os sensores x3 e x4 detectarem colisão.
5. O motor esquerdo (y1) deverá ser desligado e o motor direito (y2) ligado reversamente, sempre que uma colisão for detectada em x2, mas não em x1.
6. O motor esquerdo (y1) deverá ser ligado reversamente e o motor direito (y2) desligado, sempre que uma colisão for detectada em x1, mas não em x2.
7. O motor esquerdo (y1) deverá ser desligado e o motor direito (y2) ligado diretamente, sempre que uma colisão for detectada em x4, mas não em x3.
8. O motor esquerdo (y1) deverá ser ligado diretamente e o motor direito (y2) desligado, sempre que uma colisão for detectada em x3, mas não em x4.

> Caso alguma condição lógica esteja presente em mais de uma instrução, considerar a primeira condição que ocorre!

<!--
1. O motor esquerdo (y1) deverá ser ligado e o motor direito (y2) desligado, permitindo que o robô rotacione em sentido horário, sempre que um objeto for detectado em x1 e/ou x3, mas não em x2.
1. O motor esquerdo (y1) deverá ser desligado e o motor direito (y2) ligado, permitindo que o robô rotacione em sentido anti-horário, sempre que um objeto for detectado em x2 e/ou x3, mas não em x1.
1. Ambos os motores devem ser ligados se nenhum dos sensores detectar um objeto ou se x1 e x2 detectarem o objeto.
1. Todos os motores devem ser desligados se os três sensores detectarem um objeto.
-> Caso alguma condição lógica esteja presente em mais de uma instrução, considerar a primeira condição que ocorre!
-->



## Rubricas

| Conceito | Descritivo                                                  |
|----------|-------------------------------------------------------------|
| **A+**   | Funções lógicas implementadas com transistores no protoboard                     |
|          | Anexar video no repositório da atividade                    |
| **B+**   | Funções lógicas implementadas com transistores no simulador falstad ou tinkercad |
|          | Anexar video e/ou o arquivo texto da simulação no repositório da atividade       |
| **C+**   | Funções lógicas obtidas e simplificadas                     |
|          | Anexar foto da resolução                                    |
| **D**    | Funções lógicas obtidas mas não simplificadas               |
| **I**    | Funções lógicas não obtidas                                 |

# A - Álgebra Booleana e Implementação de Funções Lógicas com CIs

| Data da entrega| 
|----------------|
| {{apsA_date}} |

Nesse projeto iremos utilizar a álgebra booleana para obter as funções lógicas de um sistema as quais deverão ser implementadas utilizando CIs.

Esse projeto deverá ser realizado em grupos de 4 integrantes e os arquivos devem ser enviados pelo Blackboard (é necessário que apenas um(a) integrante do grupo envie, desde que identifique os demais membros).

Queremos controlar o robô da figura a seguir:

![](../figs/A-Transistores/carro.png){width=400}


onde y1 e y2 são sinais de saída (de 2 bits cada) para os motores que controlam as esteiras da esquerda e direita. x1, x2, x3 e x4 são sensores (bumpers) para detectar a colisão do robô.

Os sinais de y1 e y2 (de 2 bits cada) descrevem os seguintes movimentos:

- "01" - motor ligado diretamente (andando para frente)
- "10" - motor ligado reversamente (andando para trás) 
- "00" - motor desligado

> **os sinais y1 e y2 devem ser ligados as entradas I1, I2, I3 e I4 da ponte H.**

![](../figs/A-Transistores/motor.png){width=400}

O Monte uma tabela verdade de controle do carrinho da seguinte forma:

1. Todos os motores devem ser desligados se (x1 e x2) e (x3 e x4) indicar colisão.
2. Todos os motores devem permanecer desligados se nenhum sensor indicar colisão.
3. Ambos os motores devem ser ligados reversamente se os sensores (x1 e x2) detectarem colisão.
4. Ambos os motores devem ser ligados diretamente se os sensores (x3 e x4) detectarem colisão.
   
5. O motor esquerdo (y1) deverá ser ligado e o motor direito (y2) desligado, permitindo que o robô rotacione em sentido horário, sempre que um objeto for detectado em x1 e/ou x3, mas não em x2.
6.. O motor esquerdo (y1) deverá ser desligado e o motor direito (y2) ligado, permitindo que o robô rotacione em sentido anti-horário, sempre que um objeto for detectado em x2 e/ou x3, mas não em x1.
7. Ambos os motores devem ser ligados se nenhum dos sensores detectar um objeto ou se x1 e x2 detectarem o objeto.
8. Todos os motores devem ser desligados se todos os sensores detectarem um objeto.
Caso alguma condição lógica esteja presente em mais de uma instrução, considerar a primeira condição que ocorre!




## Rubricas

| Conceito | Descritivo                                                  |
|----------|-------------------------------------------------------------|
| **A+**   | Funções lógicas implementadas com CIs no protoboard e testadas no carrinho       |
|          | Anexar video                                                |
| **B+**   | Funções lógicas implementadas com CIs no simulador falstad ou tinkercad |
|          | Anexar video e/ou o arquivo texto da simulação              |
| **C+**   | Funções lógicas obtidas e simplificadas                     |
|          | Anexar foto da resolução                                    |
| **D**    | Funções lógicas obtidas mas não simplificadas               |
| **I**    | Funções lógicas não obtidas                                 |

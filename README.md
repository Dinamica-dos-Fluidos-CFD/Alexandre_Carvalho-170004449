# Alexandre_Carvalho-170004449
Substituição da nota da prova 
Problema 1

**Problema 1:** Uma instalação de bombeamento tem apresentado problemas em uma seção de tubulação de 1 metro de comprimento e 40 mm de diâmetro. A perda de carga foi medida usando sensores de pressão, e mensurou-se uma queda de pressão de 2 Pa. A bomba que supre esta tubulação com água está operando em potência máxima. Também mediu-se a vazão deste escoamento, obtendo um valor de 0,0001 metro cúbico por segundo na saída do tubo. O projeto de CFD deve:

- Determinar se estes valores de vazão e perda de carga estão coerentes ou não, e o motivo para isto.
- Apresentar possibilidades de problemas em caso dos valores colocados acima não estarem coerentes.
- Usando a simulação apresentada, realizar um estudo paramétrico da viscosidade do fluido para avaliar se o cenário acima é normal ou não para esta instalação.

# 1.Modelagem

### 1.1 Objetivos, Requisitos e Prazo: 
	
   O projeto realizado tem o intuito de especificar um determinado problema em uma tubulação de 40mm de diâmetro e 1000mm de comprimento. Para alcançar uma solução objetiva, será feita uma simulação por intermédio de um software de Computational Fluid    Dynamics (CFD). Será necessária, também, a parametrização das grandezas físicas atuantes no perfil estudado.

   As etapas do projeto têm duração de uma semana, desde que cumpridas todas as exigências apresentadas. Podendo ser adiadas,caso hajam incongruências ao decorrer da atividade.

### 1.2 Hipóteses de Simplificação:

   Para efeitos práticos, é importante definir quais parâmetros podem ou devem ser simplificados, tanto para simplificar o processo computacional da simulação, quanto para diminuir o número de erros provenientes das simulações.

   Estruturas externas ao fluxo devem ser desconsideradas, por serem indiferentes para o cálculo do mesmo. 
  
   As paredes internas do tubo também são prescindíveis neste caso, pois a simulação avalia tudo aquilo que não é definido como uma parede, portanto, o perfil da velocidade segue os parâmetros de Navier-Stokes.
  
   A linearidade do escoamento foi adotada pois não compromete a acurácia dos cálculos e simulações neste projeto.



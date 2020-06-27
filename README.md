# Alexandre_Carvalho-170004449
Substituição da nota da prova 
Problema 1

**Problema 1:** Uma instalação de bombeamento tem apresentado problemas em uma seção de tubulação de 1 metro de comprimento e 40 mm de diâmetro. A perda de carga foi medida usando sensores de pressão, e mensurou-se uma queda de pressão de 2 Pa. A bomba que supre esta tubulação com água está operando em potência máxima. Também mediu-se a vazão deste escoamento, obtendo um valor de 0,0001 metro cúbico por segundo na saída do tubo. O projeto de CFD deve:

- Determinar se estes valores de vazão e perda de carga estão coerentes ou não, e o motivo para isto.
- Apresentar possibilidades de problemas em caso dos valores colocados acima não estarem coerentes.
- Usando a simulação apresentada, realizar um estudo paramétrico da viscosidade do fluido para avaliar se o cenário acima é normal ou não para esta instalação.

# 1.Modelagem

### 1.1 Objetivos e Prazo: 
	
   O projeto realizado tem o intuito de estudar uma situação específica em uma estação de bombeamento de água, por meio de simulações, realizadas de maneira metódica, em uma tubulação de 40mm de diâmetro e 1000mm de comprimento. Para alcançar uma solução objetiva, será feita uma simulação por intermédio de um software de Computational Fluid Dynamics (CFD).
   
   Após feita a parametrização das grandezas físicas, juntamente com as simulações computacionais, será possível apontar se existem incoerências na vazão e na perda de carga, e qual é a relevância destas características para a tubulação em si; e por meio de um estudo paramétrico da viscosidade do fluido, avaliar a normalidade do cenário suposto.
   
   As etapas do projeto têm duração de uma semana, desde que cumpridas todas as exigências apresentadas. Podendo ser adiadas, caso hajam incongruências no decorrer da atividade.
   
### 1.2 Requisitos:

   Para que tal análise seja possível, as simulações feitas deverão retornar a vazão, que poderá ser utilizada para encontrar a velocidade média do fluxo, haja vista a invariabilidade do diâmetro ao longo do tubo; deverá, também, apontar a variação de pressão, para que seja possível relacioná-la com a perda de carga e, por fim, dados relacionados à viscosidade do fluxo para a avaliação do cenário.

### 1.3 Hipóteses de Simplificação:

   Para efeitos práticos, é importante definir quais parâmetros podem ou devem ser simplificados, tanto para simplificar o processo computacional da simulação, quanto para diminuir o número de erros provenientes das simulações.

   Estruturas externas ao fluxo devem ser desconsideradas, por serem indiferentes para o cálculo do mesmo. 
  
   As paredes internas do tubo também são prescindíveis neste caso, pois a simulação avalia tudo aquilo que não é definido como uma parede, portanto, o perfil da velocidade segue os parâmetros de Navier-Stokes.
  
   A linearidade do escoamento foi adotada pois não compromete a acurácia dos cálculos e simulações neste projeto.
   
### 1.4 Finalidade do Projeto e Metodologia:

   A finalidade deste projeto é verificar a normalidade do funcionamento da seção de tubulação que foi apresentada; e estudar, a partir dos parâmetros dados da instalação de bombeamento, quais características dentre vazão, perda de carga e viscosidade apresentam-se de maneira incoerente, determinando-as.
   
   O problema apresentado pode ser determinado de diversas formas. Porém, as características apresentadas apontam que, certamente, para que se tenha uma boa visualização situacional, a metodologia de Computational Fluid Dynamics (CFD), é a mais profícua para o caso.

### 1.5 Precisão Requisitada:

Haja vista a simplicidade da geometria apresentada, a malha utilizada para que o software resolva os equacionamentos físicos envolvidos na simulação, não carece de grandes refinamentos. Consequentemente, os resultados numéricos finais apresentados, não requerem disposição além da quarta casa decimal.


<p align="center">
 Figura 1: Modelo Tridimensional do Escoamento
</p>

![asd](https://user-images.githubusercontent.com/66135034/84211748-726e4d80-aa92-11ea-9446-c48c854b744a.png)

<p align="center">
 Figura 2: Secção Transversal do Modelo
</p>

![figura 2](https://user-images.githubusercontent.com/66135034/85301101-c9eebf00-b47d-11ea-949f-cd266e63df4d.png)

<p align="center">
 Figura 3: Secção Longitudinal do Modelo
</p>

![figura 3](https://user-images.githubusercontent.com/66135034/85301107-cce9af80-b47d-11ea-82cf-6145f028891f.png)


# 2.Pré-Processamento

### 2.1 Domínio de cálculo e Geometria:
Para fins práticos, haja vista a laminaridade do fluxo e ausência de fatores que poderiam alterar esta condição, como geradores de vórtices e rebites, não é necessário o detalhamento das estruturas externas ao fluxo em si.
Fato que possibilita a simplificação da geometria sem que haja uma perda significativa da acurácia do resultado final, haja vista que em regime laminar, o fator de atrito utilizado para determinar a perda de carga, por exemplo, independe da rugosidade do meio, sendo unicamente função do número de Reynolds.

### 2.2 Tipo de malha e Método:
A geração de malha para uma simulação é importante para que se tenha um cálculo tanto preciso no que está sendo estudado, quanto viável de ser feito em um computador convencional, para esta circunstância. Portanto, uma malha hexaédrica simples e estruturada é suficiente para atender os requisitos de precisão e viabilidade.
Quanto ao método, por não haver quaisquer geometrias complexas, propriedades materiais distintas, ou esforços estruturais essenciais para o cálculo, o Método dos Volumes Finitos pode ser utilizado, pois fará os procedimentos numéricos baseados na energia, massa e quantidade de movimento em cada volume determinado.

<p align="center">
 Figura 4: Malha Hexaédrica Gerada Automaticamente
</p>

![Malha](https://user-images.githubusercontent.com/66135034/85929002-9bab1e00-b887-11ea-8bc3-b1d919fe1db9.png)

### 2.3 Inputs:
Dados a vazão volumétrica e área do fluxo, é possível obter a velocidade do mesmo, de 0,07962 m/s, como apontado pela Imagem a seguir:
 
![Velocity](https://user-images.githubusercontent.com/66135034/85929003-9c43b480-b887-11ea-82ad-7cb102a76e7b.png)

No domínio padrão, o fluxo foi caracterizado como laminar, desconsiderando transferências de calor, combustão, e radiação térmica:

![domain](https://user-images.githubusercontent.com/66135034/85929006-9c43b480-b887-11ea-9580-da58734fe9ab.png)

Como inferido pelo problema, o fluido trabalhado pela estação de bombeamento é água, e a pressão de referência adotada foi de 1 atm.

![Fluid](https://user-images.githubusercontent.com/66135034/85929007-9cdc4b00-b887-11ea-9fe4-f360de701ef4.png)
 
Foram caracterizadas, também, as superfícies do fluxo, sendo denominadas de Intake, Outlet e Wall.
 
![Vector](https://user-images.githubusercontent.com/66135034/85929001-9a79f100-b887-11ea-953b-e570fd5916ea.png)

### 2.4 Prazo e Capacidade Computacional:
Tendo em mente o prazo estipulado anteriormente, de uma semana por etapa, o processamento será feito o quanto antes, para que possam ser avaliados quaisquer desvios nos resultados.
O computador que fará o processamento da simulação conta com:

Processador: Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz 1.99 GHz.<br />
RAM instalada: 16,0 GB.<br />
Sistema operacional de 64 bits.<br />
Windows 10.<br />

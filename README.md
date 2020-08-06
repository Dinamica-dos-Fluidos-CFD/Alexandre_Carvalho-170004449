# Alexandre_Carvalho-170004449
Substituição da nota da prova 
Problema 1

**Problema 1:** Uma instalação de bombeamento tem apresentado problemas em uma seção de tubulação de 1 metro de comprimento e 40 mm de diâmetro. A perda de carga foi medida usando sensores de pressão, e mensurou-se uma queda de pressão de 2 Pa. A bomba que supre esta tubulação com água está operando em potência máxima. Também mediu-se a vazão deste escoamento, obtendo um valor de 0,0001 metro cúbico por segundo na saída do tubo. O projeto de CFD deve:

- Determinar se estes valores de vazão e perda de carga estão coerentes ou não, e o motivo para isto.
- Apresentar possibilidades de problemas em caso dos valores colocados acima não estarem coerentes.
- Usando a simulação apresentada, realizar um estudo paramétrico da viscosidade do fluido para avaliar se o cenário acima é normal ou não para esta instalação.

# 1.Modelagem

### 1.1 Objetivos e Prazo: 
	
   O projeto realizado tem o intuito de estudar um escoamento de água no interior de uma tubulação em uma estação de bombeamento, para que seja possível determinar a coerência dos dados de vazão, perda de carga e viscosidade apontados; apontando possíveis soluções para corrigir a divergência nos valores.
   
   O escoamento ocorre no interior de uma tubulação de 1 metro de comprimento e 40mm de diâmetro contendo água, cuja vazão é de 0,0001 metro cúbico por segundo, e perda de carga medida segundo uma queda de pressão de 2 Pa.
 
  A partir dos resultados provenientes da simulação e dos dados teóricos, será possível realizar uma comparação entre os dados fornecidos e encontrados, para encontrar possíveis incongruências, que serão posteriormente analisadas com o estudo paramétrico da viscosidade do fluido.
  
   As etapas do projeto têm duração de uma semana, desde que cumpridas todas as exigências apresentadas. Podendo ser adiadas, caso hajam incongruências no decorrer da atividade.
   
### 1.2 Requisitos:

   Para que tal análise seja possível, as simulações feitas deverão retornar a vazão, que poderá ser utilizada para encontrar a velocidade média do fluxo, haja vista a invariabilidade do diâmetro ao longo do tubo; deverá, também, apontar a variação de pressão, para que seja possível relacioná-la com a perda de carga e, por fim, dados relacionados à viscosidade do fluxo para a avaliação do cenário.
   
   Para alcançar uma solução objetiva, será feita uma simulação por intermédio de um software de Computational Fluid Dynamics (CFD).

### 1.3 Hipóteses de Simplificação:

   Para efeitos práticos, é importante definir quais parâmetros podem ou devem ser simplificados, tanto para simplificar o processo computacional da simulação, quanto para diminuir o número de erros provenientes das simulações.

   Estruturas externas ao fluxo devem ser desconsideradas, por serem indiferentes para o cálculo do mesmo.
  
   As paredes internas do tubo também são prescindíveis neste caso, pois a simulação avalia tudo aquilo que não é definido, como uma parede. Portanto, o perfil da velocidade segue os parâmetros de Navier-Stokes.
  
   A laminaridade do escoamento foi adotada pois não compromete a acurácia dos cálculos e simulações neste projeto.
   
   Haja vista a adoção de um escoamento laminar, a rugosidade material da tubulação torna-se despezível para o cálculo do fator de atrito.
   
### 1.4 Finalidade do Projeto e Metodologia:

   A finalidade deste projeto é desenvolver e aprimorar os conhecimentos práticos, de maneira acadêmica, na área de simulações computacionais de dinâmica dos flúidos, por meio de um projeto simples que introduz, principalmente, as ferramentas, boas práticas e hábitos adotados por um engenheiro quando realizando trabalhos dessa espécie. 
   
   Após feita a parametrização das grandezas físicas, juntamente com as simulações computacionais, será possível apontar se existem incoerências na vazão e na perda de carga, e qual é a relevância destas características para a tubulação em si; e por meio de um estudo paramétrico da viscosidade do fluido, avaliar a normalidade do cenário suposto.
   
   O problema apresentado pode ser acertado de diversas formas. Porém, as características apresentadas apontam que, certamente, para que se tenha uma boa visualização situacional, a metodologia de Computational Fluid Dynamics (CFD), é a mais profícua para o caso.

### 1.5 Precisão Requisitada:

Haja vista a simplicidade da geometria apresentada, a malha utilizada para que o software resolva os equacionamentos físicos envolvidos na simulação, não carece de grandes refinamentos. Consequentemente, os resultados numéricos finais apresentados, não requerem disposição além da quarta casa decimal.

![asd](https://user-images.githubusercontent.com/66135034/84211748-726e4d80-aa92-11ea-9446-c48c854b744a.png)
<p align="center">
 Figura 1: Modelo Tridimensional do Escoamento
</p>



![figura 2](https://user-images.githubusercontent.com/66135034/85301101-c9eebf00-b47d-11ea-949f-cd266e63df4d.png)
<p align="center">
 Figura 2: Secção Transversal do Modelo
</p>



![figura 3](https://user-images.githubusercontent.com/66135034/85301107-cce9af80-b47d-11ea-82cf-6145f028891f.png)
<p align="center">
 Figura 3: Secção Longitudinal do Modelo
</p>


# 2.Pré-Processamento

### 2.1 Domínio de cálculo e Geometria:
Para fins práticos, haja vista a laminaridade do fluxo e ausência de fatores que poderiam alterar esta condição, como geradores de vórtices e rebites, não é necessário o detalhamento das estruturas externas ao fluxo em si.
Fato que possibilita a simplificação da geometria sem que haja uma perda significativa da precisão do resultado final, haja vista que em regime laminar, o fator de atrito utilizado para determinar a perda de carga, por exemplo, independe da rugosidade do meio, sendo unicamente função do número de Reynolds.
Portanto, o domínio de cálculo adotado pode ser simplificado.

### 2.2 Características da malha e Método:
A geração de malha para uma simulação é importante para que se tenha um cálculo tanto preciso no que está sendo estudado, quanto viável de ser feito em um computador convencional, para esta circunstância. Portanto, uma malha hexaédrica simples e estruturada é suficiente para atender os requisitos de precisão e viabilidade.
Quanto ao método, por não haver quaisquer geometrias complexas, propriedades materiais distintas, ou esforços estruturais essenciais para o cálculo, o Método dos Volumes Finitos
será utilizado, pois fará os procedimentos numéricos baseados na energia, massa e quantidade de movimento em cada volume determinado.


![Malha](https://user-images.githubusercontent.com/66135034/85929002-9bab1e00-b887-11ea-8bc3-b1d919fe1db9.png)
<p align="center">
 Figura 4: Malha Hexaédrica Gerada Automaticamente
</p>

### 2.3 Inputs:
Dados a vazão volumétrica e área do escoamento, é possível obter a velocidade do mesmo, de 0,07962 m/s, como apontado pela Imagem a seguir:
 
![Velocity](https://user-images.githubusercontent.com/66135034/85929003-9c43b480-b887-11ea-82ad-7cb102a76e7b.png)

Também foi determinada a pressão relativa na saída do escoamento, igual a 0 Pa, simplificando o cálculo da perda de carga do sistema.

### 2.4 Processamento da solução:
Para que o software processe o cenário de maneira correta, é preciso determinar as condições de contorno.

No domínio padrão, o fluxo foi caracterizado como laminar, desconsiderando transferências de calor, combustão, e radiação térmica:

![domain](https://user-images.githubusercontent.com/66135034/85929006-9c43b480-b887-11ea-9580-da58734fe9ab.png)

Como inferido pelo problema, o fluido trabalhado pela estação de bombeamento é água, e a pressão de referência adotada foi de 1 atm.

![Fluid](https://user-images.githubusercontent.com/66135034/85929007-9cdc4b00-b887-11ea-9fe4-f360de701ef4.png)
 
Foram caracterizadas, também, as superfícies da malha do escoamento, sendo denominadas de Intake, Outlet e Wall; significando "entrada", "saída" e "parede", respectivamente.
 
![Vector](https://user-images.githubusercontent.com/66135034/85929001-9a79f100-b887-11ea-953b-e570fd5916ea.png)

Para finalizar o Pré-processamento, a aba Solver Control aponta as características de solução simulacional.
As caracteristicas determinadas foram controle e critérios de convergência, controle da escala de tempo do fluido, dentre outros:

Mínimo e Máximo de Iterações de 1 e 100, respectivamente.

Timescale Factor de 1.

### 2.5 Prazo e Capacidade Computacional:
Tendo em mente o prazo estipulado anteriormente, de uma semana por etapa, o processamento será feito o quanto antes, para que possam ser avaliados quaisquer desvios nos resultados.
O computador que fará o processamento da simulação conta com:

Processador: Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz 1.99 GHz.<br />
RAM instalada: 16,0 GB.<br />
Sistema operacional de 64 bits.<br />
Windows 10.<br />

# 3. Processamento e Pós-Processamento:

### 3.1 Histórico de convergência e tempo de processamento:


![Histórico de Convergência](https://user-images.githubusercontent.com/66135034/88740761-6149d080-d114-11ea-82bc-12b475a02785.png)
<p align="center">
 Gráfico 1: Histórico de convergência.
</p>


O histórico de convergência aponta que as características de conservação de massa e momento estão coerentes com suas realidades físicas. Portanto, os cálculos estão adequados.
Por se tratar de uma simulação simples, com baixos níveis de complexidade, o tempo de processamento foi de apenas 3.220 segundos, como apontado abaixo:
 
 
![Tempo de Operação](https://user-images.githubusercontent.com/66135034/88740763-61e26700-d114-11ea-8cb6-a68cb913c771.png)
<p align="center">
Figura 5: Tempo de processamento.
</p>

### 3.2 Resíduos simulacionais:
Os resíduos da simulação não representam, para este caso, um empecilho para o recolhimento de dados precisos, haja vista a utilização de uma malha hexaédrica suficientemente refinada, e a simplicidade da situação.

### 3.3 Resultados Qualitativos e Quantitativos:
Foi possível obter diversos resultados qualitativos derivados desta simulação, como a velocidade do escoamento e seu perfil, variação da pressão ao longo do tubo, entre outros:
 
 
![Flow Velocity](https://user-images.githubusercontent.com/66135034/88740764-627afd80-d114-11ea-8096-05b537fac613.png)
<p align="center">
Figura 6: Velocidade do escoamento.
</p>

É possível analisar o arrasto gerado pela superfície do tubo, freando o fluido que por ele escoa, nas camadas mais próximas às paredes internas.
 
 
![Velocity Profile](https://user-images.githubusercontent.com/66135034/88740765-627afd80-d114-11ea-9deb-6e5fdf4874b8.png)
<p align="center">
Gráfico 2: Perfil da velocidade do escoamento.
</p>

Este gráfico demonstra o que seria uma secção longitudinal do escoamento, é possível notar que este escoamento está conforme as descrições de Navier-Stokes.
Entretanto nota-se, também, que o perfil da velocidade se assemelha mais ao seu estado em desenvolvimento do que com o estado totalmente desenvolvido, geralmente representado por uma parábola.


![Pressure (1)](https://user-images.githubusercontent.com/66135034/88740767-63139400-d114-11ea-80dd-16eefd87b423.png)
<p align="center">
Figura 7: Variação da pressão ao longo do escoamento.
</p>


Também classificado como dado qualitativo, a figura mostra a variação na pressão que o escoamento sofreu devido à perda de carga.
Os gráficos relativos à perda de carga estão localizados no estudo paramétrico da viscosidade.

Todos os resultados simulados concordam, mesmo que com alguns resíduos, com a realidade física do escoamento.


### 3.4 Estudo Paramétrico da Viscosidade

A viscosidade, ou atrito intermolecular do fluido, influencia na perda de carga de um sistema, portanto, fluidos com viscosidades distintas causam perdas de carga diferentes, tanto pelas características do fluido em si, como por outros fatores influenciadores, como a temperatura. 

Para o estudo paramétrico da viscosidade, foram determinadas três temperaturas hipotéticas diferentes para o fluido do escoamento, e suas respectivas viscosidades, como demonstrado abaixo:


Viscosidades:

Água a 0°C --- 0.0018 Pa * s 

Água a 25°C --- 0.000889 Pa * s  

Água a 140°C --- 0.0002 Pa * s

A teoria aponta que fluidos mais viscosos sofrem maior perda de carga, e que a temperatura é inversamente proporcional à viscosidade do fluido (fluidos mais quentes tornam-se menos viscosos e vice-versa), fato que é facilmente demonstrado pelos resultados das simulações:


![Perda de Carga viscosidade a 0 0018 Pa s](https://user-images.githubusercontent.com/66135034/88740862-8f2f1500-d114-11ea-83b0-0141447e555a.png)
<p align="center">
Gráfico 3: Perda de carga no escoamento para água a 0°C.
</p>

A perda de carga do escoamento para água a 0°C, com viscosidade de 0.0018 Pa * s, foi de aproximadamente 3,8 Pa.
 
 
 
![Perda de Carga viscosidade a 0 0008899 Pa s](https://user-images.githubusercontent.com/66135034/88740865-90604200-d114-11ea-87cb-2b8c4389158a.png)
<p align="center">
Gráfico 4: Perda de carga no escoamento para água a 25°C.
</p>


A perda de carga do escoamento para água sob condições ambientais de temperatura (25°C), foi de aproximadamente 2 Pa.



![Perda de Carga viscosidade a 0 0002 Pa s](https://user-images.githubusercontent.com/66135034/88740866-90604200-d114-11ea-8b81-e21f6b178e47.png)
<p align="center">
 Gráfico 5: Perda de carga no escoamento para água a 140°C.
 </p>
 
Já a perda de carga do escoamento para água a 140°C, foi de aproximadamente 0.44 Pa.

Como dito anteriormente, o fator de atrito de um escoamento laminar depende unicamente do número de Reynolds que, por sua vez, é função da viscosidade do flúido, sendo inversamente proporcional à mesma.

![Screenshot (8)](https://user-images.githubusercontent.com/66135034/89567403-fa08dc00-d7f7-11ea-9a54-3e9c5ed58f6b.png)
<p align="center">
 Figura 8: Fator de atrito para escoamento laminar.
 </p>

![Screenshot (9)](https://user-images.githubusercontent.com/66135034/89567408-faa17280-d7f7-11ea-8060-0002178f372a.png)
<p align="center">
 Figura 9: Coeficiente de Reynolds.
 </p>
 Onde 
 
 v = Velocidade média do fluido
 
 D = Diâmetro para o fluxo no tubo
 
 μ = Viscosidade dinâmica do fluido 
 
 ρ = Massa específica do fluido

As simulações apontam que houve, de fato, uma alteração na perda de carga do escoamento dada a variação da viscosidade do fluido e endossam, portanto, os conhecimentos físicos teóricos que apontavam que tal variação causaria uma modificação no fator de atrito do escoamento e, por fim, alteranto a perda de carga em si.
 
# 4. Conclusão:

O intuito do projeto, de relacionar conhecimento teórico e técnicas de CFD, é muito interessante para a introdução dos alunos no mercado atual de trabalho. É imprescindível que exista harmonia entre a teoria, conhecimentos físicos, e resultados obtidos por meio das simulações; para que seja possível analisar a validade das simulações e, com isso, usufruir das facilidades práticas que elas possibilitam. 

O projeto realizado por meio do Ansys possibilitou não só a realização dos complexos cálculos que regem os fluidos, como também uma boa visualização geral do cenário apresentado, apontando diversos dados quantitativos e qualitativos que tornaram possível a avaliação do problema estudado.


---
title: Desempenho da aeronave Embraer 145LR
description: Esse foi um trabalho apresentado a disciplina de Desemepnho de aeronaves na época de graduação em enegnharia aeronáutica
author: Guilherme Aguiar Brum
date: 2019-08-08 11:33:00 +0800
categories: [Blogging, Demo]
tags: [typography]
pin: true
math: true
mermaid: true
image:
  path: https://www.airway.com.br/wp-content/uploads/2020/08/emb-145-primeiro-voo.jpg
  alt: EMB-145

---
## 1.  Uma breve história sobre o EMB-145 

A evolução do mercado no final dos anos 1980 provocou discussões acaloradas sobre os novos conceitos usados na aviação regional. Os passageiros demonstravam uma aversão cada vez maior aos turboélices, exatamente quando crescia a demanda por viagens regionais de curta distância. Uma Nova Era, era marcada por motores a jato, surgia no Horizonte.

Em 1989, a Embraer decidiu entrar no mercado relativamente novo, mas em rápido crescimento, de jatos regionais. Essa decisão revelou-se um passo estratégico decisivo, uma vez que o mercado para suas aeronaves turboélices encontrava-se numa fase de declínio que só fez se afundar nos anos subsequentes. Os jatos têm a capacidade de voar a velocidades maiores e acima da turbulência, proporcionando maior conforto para os passageiros. A Comair, empresa baseada nos Estados Unidos e importante operadora do EMB 120, contratou a Embraer para discutir a possibilidade de operar um jato na faixa de 50 passageiros. A Embraer respondeu ao chamado do mercado, por aviões maiores e mais rápidos acionados por motores turbofan e caracterizados por custos operacionais mais baixos, lançando o EMB 145, mais tarde denominado RJ 145. O avião surgiu pela primeira vez nas pranchetas do desenho da Embraer em 1988, durante o período do desenvolvimento do CBA 123.

Em seu conceito original, RJ-145 era uma versão a jato do Brasília ampliado para acomodar 45 lugares em vez de 30 passageiros. Os desenhos iniciais previam a instalação de turbinas em baixo de cada uma das asas em substituição aos motores turboélices do Brasília. O jato poderia ser equipado quer com sistema aviônico padrão do Brasília quer com aviônica totalmente digital do high tech CBA 123.

Projetista e engenheiros esperavam reduzir os custos lançando mão da estrutura e de componentes comuns aos 2 aviões o que também permitiria potencialmente acelerar a produção. Os custos de produção para o novo jato foram estimados em USS 300 milhões.
Testes desenvolvidos no túnel de vento na sede da Boeing revelaram que o RJ 145 segundo suas especificações originais jamais satisfaria os objetivos da Embraer de modo que a companhia decidiu redesenhar aeronave. Uma asa totalmente nova foi projetada e o motor a jato foi deslocado para baixo da asa como no Boeing 737.

Essas modificações, contudo, revelaram ser insuficientes. O projeto da aeronave teve de passar por novas modificações. Para reduzir os custos associados a necessidade de um trem de pouso maior e para acomodar as portas e escadas reprojetadas para passageiros, ao mesmo tempo em que se ampliava fuselagem para comportar essas mudanças, os projetistas optaram por deslocar os motores na fuselagem posterior, próximo à cauda como no Sud Aviation SE 210 Caravelle e no Boeing 727. Com isso, o preço por unidade fabricada passou a ser USS 23.5 milhões.

## 2. Coeficiente de Arrasto Parasita ($C_{D_0}$)

As análises de desempenho de uma aeronave são baseadas na precisão do cálculo do $C_{D_0}$. O método no qual iremos calcular o arrasto parasita do EMB-145LR é baseado na técnica de acumulação, que consiste em calcular todos componentes que contribuem para o arrasto da aeronave. 

No final todos os $C_{D_0}$ são somados e temos o coeficiente de arrasto parasita da aeronave global.Para o cálculo do arrasto parasita da aeronave $C_{D_0}$, comumente chamado de coeficiente de arrasto de sustentação zero, determinaremos alguns parâmetros da aeronave como o Fator de eficiência Aerodinâmica ou Oswald's Factor ($e$), coeficiente de arrasto induzido($K$) e Razão de Aspecto($AR$) que serão utilizados no cálculo da polar de arrasto para as condições: limpa, decolagem e de pouso no decorrer desse trabalho.

## 2.1 Fator de Oswald ($e$)

Para determinação do fator de Oswald seguimos o método usando os parâmetros geométricos básicos conforme [^Sadraey]. Dessa maneira para encontrar o fator de Oswald para o EMB-145LR usamos a seguinte formulação matemática :

$$
\begin{equation}
 e=e_{theo}\cdot k_{e,F}\cdot k_{e,D_{0}} \cdot k_{e,M}  
\end{equation}
$$
 Onde :


 $e_{theo}$ (Fator de Oswald Teórico para  arrasto invíscido devido apenas a sustentação.)

 $k_{e,F}$ (Fator de Correção para perdas na fuselagem.)

 $k_{e,D_{0}}$ (Fator de Correção para arrasto viscoso devido a sustentação.)

 $k_{e,M}$ (Fator de Correção para efeitos de Compressibilidade no arrasto induzido)

## 2.1.1 Cálculo do fator de Oswald teórico ( $e_{theo}$ )

Conforme as dimensões da aeronave EMB-145LR temos que :

Razão de Aspecto($AR$) = 7,84

Afilamento( $\lambda$ ) = 0,254

Enflexamento em 25% da corda ($\Lambda_{c/4}$)= 22.73°

$$
\begin{equation}
 e_{theo}=\frac{1}{1+f(\lambda-\Delta\lambda)\cdot AR}
\end{equation}
$$

$$
\begin{equation}
\Delta\lambda=-0,357+0,45\cdot e^{-0,0375\cdot \Lambda_{c/4}}
\end{equation}
$$

$$
\begin{equation}
 f(\lambda-\Delta\lambda)=0,0524(\lambda-\Delta\lambda)^{4} -0,015(\lambda-\Delta\lambda)^{3}+0,1659(\lambda-\Delta\lambda)^{2}-0,0706(\lambda-\Delta\lambda)+0,0119  
\end{equation}
$$

Calculando-se os termos (3) e (4) e posteriormente substituindo em (2) encontramos :

$e_{theo}= 0,9844$

## 2.1.2 Cálculo do fator de correção para fuselagem ($k_{e,f}$)

O fator de correção para fuselagem é dado da seguinte maneira :

$$
\begin{equation}
k_{e,f}= 1-2\left(\frac{d_f}{b}\right)^{^2}  
\end{equation}
$$

 Onde :

$d_{f}$ = Diâmetro da Fuselagem

$b$ = Envergadura da Asa

Para o EMB-145LR consideramos:


$d_{f}=2,4m$

$b=20,01m$

Substituindo os valores na equação (5) encontramos :

$K_{e,f}=0,9741$

## 2.1.3 Cálculo do fator de correção para Arrasto viscoso ( $k_{e,D_{0}}$ )

Para esse fator de correção usaremos a tabela abaixo, retirada em [^Oswald] :

| Categoria de Aeronave | $\dfrac{d_f}{b}$ | $k_{e,f}$ | $k_{e,D0}$ |
| :-------------------- | ----------------:| ---------:| ----------:|
| Jato                  | 0,116            | 0,973     | 0,873      |
| Jato Particular       | 0,120            | 0,971     | 0,864      |
| Turboélice            | 0,102            | 0,979     | 0,804      |
| Aviação Geral         | 0,119            | 0,971     | 0,804      |

A aeronave EMB-145LR se enquadra na categoria de aeronaves a jato, portanto usaremos :

$k_{e,D_{0}}=0,873$

Cálculo do fator de correção para efeitos de compressibilidade ( $k_{e,M}$ )

O fator de correção para efeitos de compressibilidade leva em conta o número de Mach conforme a equação abaixo:
$$
\begin{equation}
k_{e,M}= a_{e}(\frac{M}{M_{comp}}-1)^{b_{e}}+ c_{e}
\end{equation}
$$

Onde :

$a_{e}=-0,00152$

$b_{e}=10,82$

$c_{e}=1$

$M_{comp}=0,3$

$M=0,6$


Fazendo as devidas substituições encontramos um valor de:

$k_{e,M}=0,9985$


Destacamos que apesar da aeronave voar em M 0,78 usamos um M 0,60 pois a inflûencia do número de Mach no fator de Oswald aumenta bastante após M 0,6, e isso traria imprecisão no cálculo estimado do fator de Oswald, a seguir mostramos como a inflûencia do número de Mach impacta sobre o fator de Oswald para o EMB-145LR, a figura abaixo indica a região onde o fator não varia com Mach, porém no regime transônico ocorre signifcativa alteração.
      
![Gráfico Fator de Oswald X Mach](https://drive.google.com/file/d/1yuMpLqIbsyjZMLpAlv1VZPAY5nmQh68q/preview){: width="972" height="589" }


## 2.1.5 Cálculo do fator de Oswald ($e$)

Após calculados os fatores de correção, usamos a equação (1) para o cálculo do fator de oswald estimado para o EMB-145LR.

$$
    \begin{align*}
e&=e_{theo}.k_{e,F}.k_{e,D_0}.k_{e,M}
\end{align*}
$$

$$
\begin{align*}
e&= 0,9844. 0,9741. 0,873. 0,9985
\end{align*}
$$

$$
\begin{align*}
e&= 0,8358\
    \end{align*}
$$


O valor encontrado é aceitável uma vez que de acordo com [^Raymer] aeronaves com razão de aspecto entre 7 e 9 estão dentro dessa faixa de fator de Oswald.

## 2.2 Cálculo do Coeficiente de Arrasto Induzido ($K$)
O coficiente de arrasto induzido $K$ está associado ao arrasto induzido, sendo esse o arrasto produzido pelos componentes que geram sustentação na aeronave, sendo calculado da seguinte maneira:

$$
 \begin{equation}
    K= \frac{1}{\pi.e.AR}
\end{equation}
$$

Substituindo os valores em (7) teremos :

$$
\begin{align*}
 k&=\frac{1}{3,14\cdot0,8358\cdot7,84} 
\end{align*}
$$

$$
\begin{align*}
 k&=0,0485
 \end{align*}
 $$

## 2.3 Cálculo do Coeficiente de Arrasto Parasita da Aeronave ($C_{D_0}$)

Conforme dito, o método utilizado para determinação do $C_{D_0}$ da aeronave será o método da acumulação, conforme a equação abaixo:

$$
\begin{equation}
C_{D_0}=C_{D_{0_f}}+C_{D_{0_w}}+C_{D_{0_{ht}}}+C_{D_{0_{vt}}}+C_{D_{0_{LG}}}+C_{D_{0_N}}+C_{D_{0_S}}+C_{D_{0_{HLD}}}+ ...
\end{equation}
$$

Onde :

$C_{D_{0_f}}$ Coeficiente de arrasto parasita da Fuselagem

$C_{D_{0_w}}$ Coeficiente de arrasto parasita da Asa

$C_{D_{0_{ht}}}$ Coeficiente de arrasto parasita da Empenagem Horizontal

$C_{D_{0_{vt}}}$ Coeficiente de arrasto parasita da Empenagem Vertical

$C_{D_{0_{LG}}}$ Coeficiente de arrasto parasita do Trem de Pouso

$C_{D_{0_N}}$ Coeficiente de arrasto parasita da Nacele

$C_{D_{0_S}}$ Coeficiente de arrasto parasita do Strut

$C_{D_{0_{HLD}}}$ Coeficiente de arrasto parasita de Dispositivos Hiper Sustentadores


## 2.3.1 Coeficiente de arrasto parasita da fuselagem ($C_{D_{0_f}}$ )

O coeficiente de arrasto parasita da Fuselagem é dado pela seguinte equação :

$$
\begin{equation}
 C_{D_{0_f}}=C_{f_f} f_{LD} f_M\frac{S_{wet_f}}{S}
\end{equation}
$$

- $C_{f_f}$ é o coeficiente de fricção  de fusleagem, que é definido pelo coeficiente de fricção da relação de Prandtl 


$$
\begin{equation}
    C_{f}=\frac{0,455}{[log_{10}(Re)]^{2,58}}\ \ \ \ \ \ \ \ \ \ \text{(Fluxo Turbulento)}   
\end{equation}
$$

$$
\begin{equation}
    C_{f}=\frac{1,327}{\sqrt{Re}} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \text{(Fluxo Laminar)}
\end{equation}
$$

Para determinar o coeficiente de fricção para fuselagem calculamos antes o número de Reynolds.
O admimensional $Re$ é dado pela seguinte relação :
$$
\begin{equation}
    Re=\frac{\rho V L}{\mu }
\end{equation}
$$

Onde :

$\rho$: Densidade do ar Local

$V$: Velocidade verdadeira da aeronave

$\mu$: Viscosidade dinâmica do ar

$L$: Comprimento da fuselagem



Para $Re$ $<$ 200.000 adotaremos o fluxo como laminar e para $Re$$>$ 2.000.000 adotaremos o fluxo como turbulento

Considerando que a aeronave voa em maior parte da missão no seu nível de voo de cruzeiro, iremos estimar nosso número de Reynolds com base no FL250($\rho_{FL250}=0,5489$), uma viscosidade dinâmica do ar($\mu=2,8050\times10^{-5}$), velocidade de cruzeiro de 400 knot e um comprimento de fuselagem de $27,93 m$ :


$$
\begin{equation*}
Re=\frac{0,5489\cdot(400\cdot0,5144)\cdot 27,93}{1,53826\times10^{-5}}= 2,05\times 10^{8}
\end{equation*}
$$

Ou seja, temos um Reynolds turbulento, portanto usaremos a equação(10) para determinar o Coeficiente de fricção da fuselagem baseado na relação de Prandtl tão logo ($C_{f_f}$) será:

$$
\begin{equation*}
 C_{f_f}= 0,00192
\end{equation*}
$$

- ${f_{LD}}$ é um coeficiente que relaciona o comprimento da fuselagem com o seu diâmetro, que é definido como :
$$
\begin{equation}
 {f_{LD}} =1+ \frac{60}{(L/D)^{3}}+0,0025\left(\frac{L}{D}\right) 
\end{equation}
$$


Onde:


$L$ é o comprimento da fuselagem

$D$ é o diâmetro máximo da fuslagem


Esses dados são facilmente encontrados na lista de dimensões gerais do EMB-145. Substituindo os valores temos:

$$
\begin{equation*}
{f_{LD}}   = 1,06212 
\end{equation*}
$$

- ${f_M}$ é o coeficiente que relaciona com o Número de Mach, definido como :
$$
\begin{equation}
{f_M}= 1-0,08M^{1.45}  
\end{equation}
$$

De acordo com os dados de desempenho da aeronave sabemos que a mesma voa em M = 0,78
substituindo M na equação (14) temos:
$$
\begin{equation*}
{f_M}=0,94420    
\end{equation*}
$$

 $\displaystyle{\frac{S_{wet_f}}{S}}$ É a relação entre área molhada total da fuselagem e área de referência da Asa.


A área molhada, é a área que é exposta ao escoamento de ar duarante o voo. Para determiná-lo pode-ser usar relações empíricas de aeronaves já produzidas através de tabelas ou pode-se usar softwares CAD para estimar com mais precisão a área molhada de cada componente da aeronave. Para nosso trabalho usamos um modelo CAD do embraer 145 disponível para {https://grabcad.com/library/embraer-erj-145-1}, conforme imagem e tabela abaixo:


![EMB-145 SolidWorks](https://drive.google.com/file/d/1FRDOWGzvFCzfennFSBA2TkiuJ-2W0q7j/preview){: width="972" height="589" }





| Componente             | Nomenclatura          | Área ($m^2$) |
| :--------------------- | :-------------------- | -----------: |
| Fuselagem              | $S_{wet_f}$           | 190,00       |
| Asa                    | $S_{wet_w}$           | 87,00        |
| Empenagem Vertical     | $S_{wet_{vt}}$        | 24,28        |
| Empenagem Horizontal   | $S_{wet_{ht}}$        | 24,72        |
| Nacele                 | $S_{wet_n}$           | 18,00        |
| Pylone                 | $S_{wet_{pl}}$        | 6,70         |
| **Total**              | $S_{wet}$             | **350,00**   |


Sabendo que a área de referência da asa é de $51,18 m^2$ temos todos os valores necessários para determinar o coeficiente de arrasto parasita da fuselagem, substituindo os valores encontrados na equação (9) temos:
$$
\begin{equation*}
\begin{align*}
    C_{D_{0_f}}&=0,00192\cdot1,06212\cdot0,94420\cdot\left(\frac{190}{51,18}\right)\\
    C_{D_{0_f}}&=0,007148
\end{align*}
\end{equation*}
$$


















## Referências

[^Sadraey]: Aircraft performance An Engineering Approach- Sadraey
[^Oswald]:Estimating the Oswald factor from basic aircraft geometrical parameters- Mihaela and Scholz, Dieter
[^Raymer]: Aircraft Design: a conceptual approach- Raymer, Daniel
 
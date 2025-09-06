---
title: Modificação em Joystick
description: Aumentando a precisão de um joystick para simular voos em simuladores de voo
author: Guilherme Aguiar Brum
date: 2019-05-22 09:33:00 +0800
categories: [Projetos Caseiros]
tags: [DIY]
pin: true
math: true
mermaid: true
image:
  path: https://www.leobodnar.com/shop/images/2BU0836A.jpg
  alt: Placa HUD USB da leobodnar modeleo BU0836A

---

Como um bom apreciador de simuladores de voo que sou, zelo bastante pelo realismo e imersão dentro dos simuladores de voo. De forma a aumentar a precisão e sensação de realismo ao pilotar um aeronave no computador, decidi por adquirir um SAITEK Pro Flight Yoke ![Desktop View](https://www.logitechstore.com.br/media/catalog/product/cache/105e6f420716e0751863c4b81f527d17/s/a/saitek_flight_yoke_system_5_.png){: .right }{: width="300" height="300" }. Percebi que o mecanismo interno do Joystick era composto por molas, de modo que ao soltar os comandos a força elástica das molas fazia com que os comandos voltassem para o centro. No entanto acho bastante bruto esse movimento e pouco realista. Visando buscar uma maior fluidez nos comando, encontrei em fóruns gringos uma modificação para esse Joystick da saitek. Consiste em remover as molas, e substituir por elásticos, aqueles que usamos para prender folhas, ou coisas do dia-dia. Não satisfeito na modificação, decidi mudar a resolução dos comandos. Basicamente um joystick funciona da seguinte maneira.


Um potenciômetro é acoplado aos eixos do controle para capturar os movimentos de empurrar o joystick (arfagem da aeronave) e girar o joystick (rolagem da aeronave). Dessa maneira ao variar o cursor do Joystick o potenciômetro varia sua resistência interna e através de um conversor analógico digital(ADC) transforma essa variação de resistência elétrica em tensão que é lido pela placa do Joystick. Quanto maior a resolução do ADC maior a precisão de movimento terá o joystick.

Por exemplo, um  joystick que possui uma placa com ADC de 10 bits possui $ 2^{10} =1024$ passos de resolução, enquanto que $ 2^{12}=4096$ passos. Ou seja ele captura pequenos movimentos no eixo do joystick tornando-o mais preciso nos controles.
O esquema de ligação dos potenciômetros na placa é de certo modo bastante simples , basta observar a imagem que é bastante institutiva . Temos três pinos na saída do potênciomêtro:

![Desktop View](https://www.leobodnar.com/shop/images/2BU0836A_06.jpg){: .right }{: width="300" height="300" }

1-	GND

2-	Sinal

3-	Positivo


![Desktop View](https://www.leobodnar.com/shop/images/2BU0836A_09.jpg){: width="300" height="300" }_Representação dos eixos na pinagem da placa_

Devemos ligá-los nos terminais da placa Leobodnar conforme imagem. Após isso basta ligar o joystick na entrada usb do seu pc por uma cabo USB A to B, usado em impressoras antigas, comumente encontrado em lojas de TI. O cabo USB fornecerá a alimentação 5V para placa e fará a comunicação entre os potenciômetros e o PC.

![Desktop View](assets/img/joystick1.png){: width="500" height="500" }_Esquema de ligação dos potenciômetros na placa_


![Desktop View](assets/img/joystick2.png){: width="500" height="500" }_Identificação dos potênciômetros no Joystick_



A seguir deixo o video exemplificando os processos descritos acima, e o movimento de controle do  Joystick.

{%
  include embed/video.html
  src='/assets/img/screen-20250906-130637.mp4'
  types='mp4'
  poster='/assets/img/joystick2.png'
  title='Funcionamento e mecanismo de movimentação do Joystick com a placa 2BU0836A '
  autoplay=true
  loop=true
  muted=true
%}
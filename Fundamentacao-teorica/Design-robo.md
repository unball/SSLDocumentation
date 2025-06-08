# Design do robô

Rascunho: 

Regras da competição (https://robocup-ssl.github.io/ssl-rules/sslrules.pdf ) 

Tamanho 

O robô deve caber dentro de um cilindro com 0.18m de largura e 0.15m de altura 

 

Cores do casco 

As cores devem ser as mesmas para todos os robôs sendo em um esquema de cor clara e cor escura 

A cor deve cobrir ao menos 6cm da altura máxima do robô 

O casco não pode ser refletivo para não interferir na visão 

As cores não podem ser próximas das cores usadas nos padrões da visão e bola 

As cores não podem sair durante os jogos 

 

Ações do robô 

O robô deve se movimentar no campo, respondendo aos eventos 

Para participar do mundial, o robô deve chutar a bola 


que precisamos fazer? 

Robô pro SSL 

TODO: Detalhar o que o robô do SSL faz 

 

Quais desafios teremos ao fazer o robô? 

Referência das perguntas: Introduction to autonomous robots  

 

Como ele se move?  

Onde o robô irá se locomover: campo. O campo é plano e coberto por carpete 

Ele deve ir para qualquer direção em qualquer instante. Mas não deve ir para fora do campo 

O robô é capaz de chutar a bola 

Obs.: Como ele chuta a bola? Quando ele chuta a bola? 

Como a velocidade das rodas afeta sua posição e velocidade no mundo?  

Aqui definimos a [cinemática do robô](https://unbbr.sharepoint.com/:o:/s/Entrevistas-UnBall/EhH6x0Or2sNPjVt3-E4rKT8BW7uh3NRbT1x5QFI9a9FwIw?e=xoFoV1) 

Como podemos controlar a velocidade das rodas para atingir uma determinada posição? 

Para isso vamos usar a cinemática do robô em conjunto com a geração e controle de sua trajetória. O Software da Equipe irá cuidar da trajetória e o robô fica responsável por apenas se movimentar até o ponto que o Software delimitar 

Quais sensores o robô usará pra perceber seu próprio estado no mundo? 

Câmera posicionada acima do campo 

Como extrair informações de seus sensores? 

Visão computacional 

Como o erro da sua percepção no mundo pode ser representado e como lidar diante de situações incertas? 

O erro é tratado no sistema de navegação (parte da estratégia). E quem vai lidar com situações adversas será o sistema de Estratégia. O robô recebe apenas para onde ir e o que fazer, ele não tem autonomia por si só. Quem envia os comandos é o computador que executa o Software da Equipe
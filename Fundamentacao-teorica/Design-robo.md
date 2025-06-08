# Design do robô

## Limitações no design advindas das regras do SSL

### Tamanho 

- O robô deve caber dentro de um cilindro com 0.18m de largura e 0.15m de altura 

### Cores do casco 

- As cores devem ser as mesmas para todos os robôs sendo em um esquema de cor clara e cor escura 
- A cor deve cobrir ao menos 6cm da altura máxima do robô 
- O casco não pode ser refletivo para não interferir na visão 
- As cores não podem ser próximas das cores usadas nos padrões da visão e bola 
- As cores não podem sair durante os jogos 

### Ações do robô 

- O robô deve se movimentar no campo, respondendo aos eventos 
- Para participarmos de competições mundiais, o robô deve chutar a bola 

## Design robô SSL - UnBall

Para facilitar o desenvolvimento do robô, foram definidas etapas para elaborar cada ação que o robô deve fazer no campo quando receber as ações da Estratégia:

### Sistema de Movimentação do Robô

Diz respeito a como o robô vai se movimentar no campo. Para isso, precisamos definir:

- Qual motor usar e como acionar com velocidade desejada?
    - [Estudo do motor](./Motor/Motor.md)
    - [Estudo de como acionar o motor](./Motor/Acionamento-Motor.md)
- Qual roda usar?
    - [Estudo de rodas para robôs omnidirecionais](./Rodas/Estudo-tipo-rodas.md)
- Como transformar a velocidade das rodas na velocidade do robô?
    - [Levantamento da cinemática do robô](./Cinematica/Cinematica-robo.md)
- Como o robô vai saber o que deve fazer?
    - [Comunicação do robô com a Estratégia](./Comunicacao/Comunicacao.md)

### Sistema de Chute

<!-- TODO: incluir links para o sistema de chute -->
Diz respeito a funcionalidade do robô de poder "chutar" a bola. Para isso, precisamos definir:

- Mecânica
- Sistema elétrico
- Quando o chute vai atuar?

## Referência

<!-- TODO: arrumar referencia pro livro -->
Buscamos responder as seguintes perguntas do livro _Introduction to autonomous robots_: 

- Como ele se move?
    > R.: Ele pode ir para todas as direções.

- Onde o robô irá se locomover?
    > R.: Em um carpete que será posicionado em cima de uma superfície plana. As dimensões do carpete segue as regras da categoria SSL 

- Como a velocidade das rodas afeta sua posição e velocidade no mundo?  
    > R.: Aqui definimos a cinemática do robô. Isso é detalhado no arquivo [Cinemática](./Cinematica/Cinematica-robo.md)

- Como podemos controlar a velocidade das rodas para atingir uma determinada posição? 
    > R.: Aqui definimos a forma como vai funcionar a Navegação do Robô. Isso é feito na Estratégia. Os detalhes da Estratégia como qual método de navegação vamos usar e qual sistema de decisão vamos aplicar pode ser visto em [Navegação](./Estrategia/Navegacao.md) e [Decisão](./Estrategia/Decisao.md), respectivamente.

- Quais sensores o robô usará pra perceber seu próprio estado no mundo? 
    > R.: A princípio, somente as câmeras posicionadas acima do campo. 

- Como extrair informações de seus sensores?
    > R.: Através do Sistema de Visão Computacional Unificado gerido pela organização da categoria SSL. 

- Como o erro da sua percepção no mundo pode ser representado e como lidar diante de situações incertas? 
    > R.: Isso vai ser detalhado em [Navegação](./Estrategia/Navegacao.md) e [Decisão](./Estrategia/Decisao.md).

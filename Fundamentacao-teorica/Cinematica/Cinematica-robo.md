# Cinemática

## Definir configuração das rodas do robô

### Possíveis configurações do robô omnidirecional 
 
Vamos trabalhar com robôs holonomicos

Não tem restrição de movimento. Ele pode ir para qualquer lugar a qualquer instante. Pode ter 3 rodas ou 4 rodas 

3 rodas tem que seguir a seguinte configuração: 

Três rodas omni montadas em uma configuração triangular com seus eixos inclinado em 120 graus em relação entre si 

![3-rodas](3-rodas.png)

4 rodas pode ser 

Rodas omni simétricas em 90 graus. Configuração '+' em b e 'x' em c. 
![dois tipos de omni com 4 rodas](4-rodas.png)

Rodas mecanum como se fosse um carro 
![carro](mecanum.png)

Comparação entre 3 rodas e 4 rodas em 'x' 

Referências: Modeling and Assessing of omni-directional robots with three and four wheels 

|  | Número de rodas | Tipo de rodas | Prós pro SSL | Contras pro SSL |
|---|---|---|---|---|
| Omni | 3 | Omni | Cria 3 pontos de contato (um plano) com mesma pressão nas rodas. Precisa de menor corrente pra atingir velocidade máxima que 4 rodas | Aceleração menor que 4 rodas |
| Omni | 4 | Omni | Aceleração bem mais rápida | Consome mais potência. Pode precisar de suspensão pra compensar a roda que fica suspensa e garantir pressão igual nas rodas que ficam no chão |
| "Carro" | 4 | Mecanum |  | Pode não caber bem dentro do cilindro limite da categoria. Qualquer espaço é sagrado |

Obs.: É possível usar rodas mecanum em robôs omni na configuração de 3 rodas e 4 rodas. Porém a roda mecanum pode gerar uma limitação na movimentação do robô que deve ser considerada no projeto do controle do robô. Também não achei exemplos usando algo assim, então pra ter certeza que funcionaria no SSL teria que fazer algum estudo ou uma bateria de testes primeiro. [Maria Claudia] 

### Configuração escolhida e justificativa 
![4 rodas omni](config-chute.png)

Motivo: 

Tem espaço pro sistema de chute, como na seta vermelha 

Permite "esconder" as rodas com a camisa do robô  

Aceleração maior com 4 rodas = mais rápido para chegar na bola, pra defender a área aliada, etc 

## Formulação matemática
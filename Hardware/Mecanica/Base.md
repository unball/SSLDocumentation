# Design

Possíveis configurações do robô omnidirecional 
 
Definimos que vamos trabalhar com robôs holonomicos 

Não tem restrição de movimento. Ele pode ir para qualquer lugar a qualquer instante. Pode ter 3 rodas ou 4 rodas 

3 rodas tem que seguir a seguinte configuração: 

Três rodas omni montadas em uma configuração triangular com seus eixos inclinado em 120 graus em relação entre si 

![GetImage](https://github.com/user-attachments/assets/6901240e-364a-4afb-a31f-8f17f4cec243)

4 rodas pode ser 

Rodas omni simétricas em 90 graus. Configuração '+' em b e 'x' em c. 
![GetImage (1)](https://github.com/user-attachments/assets/8142ef46-3784-41b6-bbf2-28d2a6193def)

Rodas mecanum como se fosse um carro 
![GetImage (2)](https://github.com/user-attachments/assets/2418bb9e-3fdb-48e9-8a99-8db426637548)

Comparação entre 3 rodas e 4 rodas em 'x' 

Referências: Modeling and Assessing of omni-directional robots with three and four wheels 

<html>
<body>
<!--StartFragment-->
  | Número de rodas | Tipo de rodas | Tem exemplo? | Prós pro SSL | Contras pro SSL
-- | -- | -- | -- | -- | --
Omni | 3 | Omni | Sim | Cria 3 pontos de contato (um plano) com mesma pressão nas rodas. Precisa de menor corrente pra atingir velocidade máxima que 4 rodas | Aceleração menor que 4 rodas
Omni | 4 | Omni | sim | Aceleração bem mais rápida | Consome mais potência. Pode precisar de suspensão pra compensar a roda que fica suspensa e garantir pressão igual nas rodas que ficam no chão
"Carro" | 4 | Mecanum | Sim | [Maria Claudia]: Pra categoria não consigo pensar em prós agora | Pode não caber bem dentro do cilindro limite da categoria. Qualquer espaço é sagrado

<!--EndFragment-->
</body>
</html>

Obs.: É possível usar rodas mecanum em robôs omni na configuração de 3 rodas e 4 rodas. Porém a roda mecanum pode gerar uma limitação na movimentação do robô que deve ser considerada no projeto do controle do robô. Também não achei exemplos usando algo assim, então pra ter certeza que funcionaria no SSL teria que fazer algum estudo ou uma bateria de testes primeiro. [Maria Claudia] 

Configuração escolhida e justificativa 
![GetImage (3)](https://github.com/user-attachments/assets/777a16cf-a247-4b35-9834-d265fa6ed23a)

Motivo: 

Tem espaço pro sistema de chute, como na seta vermelha 

Permite "esconder" as rodas com a camisa do robô  

Aceleração maior com 4 rodas = mais rápido para chegar na bola, pra defender a área aliada, etc 

# Modelo 3D
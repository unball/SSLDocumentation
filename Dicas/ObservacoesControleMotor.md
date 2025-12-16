# Comentários a respeito do projeto do Controle do Motor GM4108120T com MKS ESP32 DUAL FOC V1.0

## Sobre o driver

### Desvantagens

Não consegue lidar bem com pico de corrente.

Não suporta execução sem limite de corrente.

Sensor de corrente é horrível.

Esp32 ser embutida só trouxe prejuízo. Fica muito dificil de corrigir em hardware os problemas com o sensor de corrente.

Não consegue lidar bem aplicando carga no motor.

Não consegue lidar bem com mau contato no encoder. 

O fusível de proteção queima porém outro componente também queima junto. Não parecia proteger nada.


## Sobre o motor

### Vantagens

É uma opção mais barata que até onde foi usada, se mostrou suficiente.

### Desvantagens

Fabricante chinesa não fornece todas as especificações importantes pro controle do motor. Muitos parâmetros foram assumidos.

O motor sem encoder, vem sem o ímã direcional no eixo.


## Sobre SimpleFOC

### Vantagens

A abstração do FOC em código realmente ajudou a entender melhor como controlar o motor BLDC. 
Seguindo a documentação, é fácil de configurar para usar com o MKS ESP32 DUAL FOC V1.0

### Desvantagens

O uso de tecnicas pra melhorar o controle pode ficar bem engessado pela biblioteca. Se quiser incluir um filtro passa-baixas ou implementar outro controlador, tem que mexer no código fonte da biblioteca

A biblioteca assume que a frequência do loop() do microcontrolador é suficiente pra considerar a discretização do controle como algo contínuo e dá pra sentir como assumir isso deu problemas na prática. Se fosse outra aplicação, menos focada na velocidade do motor, talvez assumir isso não tenha tanto impacto.

# Firmware

Arquitetura 

 

Legenda 

Sistema Central 

Onde fica a inteligência do robô. Vai receber a velocidade (em rad/s ou rpm, depende do que o controle decidir) que o robô deve ter naquele momento e repassar a velocidade para os motores. Também vai receber quando o robô deve fazer o chute 

Comunicação entre microcontroladores 

A comunicação é feita por fio, utilizando o protocolo I2C 

Sistema Periférico 

Não é a parte inteligente mas realiza os cálculos necessários para transformar a velocidade recebida do computador em tensão para as fases do motor. Como o motor é BLDC, precisa de um algoritmo de controle de rotação mais complexo que apenas mandar a tensão para o motor. Para que a rotação seja mais precisa, utilizamos a leitura do encoder que está no motor. 

Comunicação entre driver e motores 

É apenas um fio que envia a tensão de cada fase do motor para que ele gire corretamente 

Motores 

São os motores BDLC. Neles estão acoplados os encoders, que enviam a leitura da posição angular do motor para o Periférico 

Encoders 

São os fios de alimentação do encoder e também de transferência dos dados lidos para o Periférico 



Comentários: 
 

No diagrama é possível ver que há dois sistemas: 1) Central e 2) Periférico.  

 

No Sistema Central, temos uma ESP32 WROOM.  
 
No Sistema Periférico, também usamos ESP32 WROOM embutidas no driver MKS DUAL FOC v2.0.  

 
Cada driver comporta uma ESP e dois motores. Assim é possível executar o FOC o mais rápido possível sem que seus custos computacionais prejudique o acionamento do motor. Pelo menos essa é a ideia inicial.  


Implementação 

Arduíno & C++ 

Organização do código 

https://github.com/unball/FirmwarePerifericoSSL  

https://github.com/unball/FirmwareCentralSSL  





## Comunicação

PC -> roteador -> firmware central -> firmware periferico 


# Visão

# Estratégia
# Qual motor usar?

Para que os motores BDLC girem, não basta somente enviar a tensão ou corrente, temos que implementar um jeito de que cada fase (A, B ou C) do motor ligue na hora correta para que o rotor gire na direção e velocidade que desejamos. Se quiser entender melhor essa questão dos tipos de motores DC, recomendo os seguintes vídeos:  

 

DC Motor, How it works?  -> https://www.youtube.com/watch?v=LAtPHANEfQo

Brushless DC Motor, How it works ?  -> https://www.youtube.com/watch?v=bCEiOnuODac

Brushed Vs Brushless DC motor  -> https://www.youtube.com/watch?v=lmWpD9h7k2g

 

Esse "jeito" de "ligar" cada fase na hora correta pode ser implementado de diversas maneiras. A que vamos utilizar no projeto é o FOC (Field Oriented Control). O FOC é um algoritmo relativamente complexo e por conta disso, o driver que vamos usar vem com uma ESP32 embutida. Esse driver também vem com um circuito elétrico dedicado para o FOC. Juntos é possível enviar para o motor somente a tensão de cada fase (A, B ou C) na hora correta, fazendo com que o motor gire com uma eficiência melhor. Mais detalhes sobre FOC podem ser vistos na documentação SimpleFOC: https://simplefoc.com/ , que tenta trazer uma explicação mais amigável do FOC. Existem diversos vídeos também, como: 

 

What is FOC? (Field Oriented Control) And why you should use it! || BLDC Motor  -> https://www.youtube.com/watch?v=Nhy6g9wGHow

Field-Oriented Control  -> https://www.youtube.com/watch?v=_6-_jvZe7iA

Understanding Field-Oriented Control | Motor Control, Part 4  -> https://www.youtube.com/watch?v=YPD1_rcXBIE
 

 

---------------------------------------------- A escrever ainda: 

Como escolher um motor? 

 

Por que vamos usar BLDC? 

Durabilidade  

Maturidade de conhecimento em relação ao motor usado no VSSS 

Outras equipes usam também  

Fontes?  
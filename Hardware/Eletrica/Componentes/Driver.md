# MKS DUAL FOC V1.0

Link fabricante: https://makerbase3d.com/product/esp32-foc/?srsltid=AfmBOooP9k1y0BmLpniX1oX0SurjO4H1KHm1H5UuaNR8bcujxwjDCpm2

Codigo de teste:
https://github.com/makerbase-motor/MKS-ESP32FOC/tree/MKS-ESP32-FOC-V1.0 


Manual:
https://github.com/makerbase-motor/MKS-ESP32FOC/tree/MKS-ESP32-FOC-V1.0/User%20Manual


O driver que utilizamos é o MKS DUAL FOC v2.0. Ele foi escolhido por conta da ESP embutida. Existem outras versões do driver da mesma fabricante que podem ser usadas. Até agora, só achei v1.0, v2.0, v3.1/v3.2. A fabricante fornece documentação de cada uma com manual, esquemático e testes de rotina:  

 

MKS dual FOC v1.0: https://github.com/makerbase-motor/MKS-ESP32FOC/tree/MKS-ESP32-FOC-V1.0  

MKS dual FOC v2.0: https://github.com/makerbase-motor/MKS-ESP32FOC/tree/MKS-ESP32-FOC-V2.0  

MKS dual FOC v3.1/3.2: https://github.com/makerbase-mks/MKS-DUALFOC/tree/main 

 

Também achei esse repositório com links e documentos que podem ser úteis para gente, juntando datasheet de encoder, driver, código para o driver, etc: https://github.com/makerbase-mks/simplefoc-MKS/tree/main/02_Makerbase%20Simple%20FOC%20related%20documents  e https://github.com/makerbase-mks  
 
O SimpleFOC (https://simplefoc.com/) fornece uma biblioteca que facilita muito a implementação do FOC no arduíno. Como o MKS DUAL FOC v2.0 tem uma ESP32, é possível utilizar arduino também. Por esse motivo de ser mais amigável, sem precisar implementar o FOC do zero, vamos utilizar arduíno nessa arquitetura.  
# Ejercicios Tema 2

#### 1. Calcular la disponibilidad del sistema si tenemos dos réplicas de cada elemento (en total 3 elementos en cada subsistema).

## Disponibilidades iniciales
| Component   	| Availability 	|  
|-------------	|--------------	|
| Web         	| 85%         	|
| Application 	| 90%         	|
| Database	 	| 99.9%       	|
| DNS		 	| 98%         	|
| Firewall		| 85%         	|
| Switch	 	| 99%         	|
| Data Center 	| 99.99%      	|
| ISP		 	| 95%         	|

## Con 2 elementos en cada subsistema
| Component   	| Availability 	|
|-------------	|--------------	|
| Web         	| 97.75%       	|
| Application 	| 99%         	|
| Database	 	| 99.9999%     	|
| DNS		 	| 99.96%       	|
| Firewall		| 97.75%       	|
| Switch	 	| 99.99%       	|
| Data Center 	| 99.99%      	|
| ISP		 	| 99.75%       	|

### Ecuación para el cálculo de la disponibilidad por componente
> __As = Acn-1 + ( (1 – Acn-1) * Acn )__

##### Cálculo de la disponibilidad por componente
- Web = 97.75% + (1 - 97.75%) * 85% = 99.6625%
- Application = 99% + (1 - 99%) * 90% = 99.9%
- Database = 99.9999% + (1-99.9999%) * 99.9% = 99.9999999%
- DNS = 99.96% + (1 - 99.96%) * 98% = 99.9992%
- Firewall = 97.75% + (1 - 97.75%) * 85% = 99.6625%
- Data Center = 99.99%
- ISP = 99.75% + (1 - 99.75%) * 95% = 99.9875%

### Ecuación para el cálculo de la disponibilidad total
> __As = Ac1 * Ac2 * Ac3 * ... Acn__

##### Disponibilidad total = 99.6625% * 99.9% * 99.9999999% * 99.9992% * 99.6625% * 99.99% * 99.9875% = 99.20%      
  
#### 2. Buscar frameworks y librerías para diferentes lenguajes que permitan hacer aplicaciones altamente disponibles con relativa facilidad. 

## PHP
- [Zend](https://ww2.zend.com/en/products/server/high-availability)
- [CodeIgniter](https://codeigniter.com/)
- [CakePHP](https://cakephp.org/)

## Javascript
- [StrongLoop API Gateway](https://strongloop.com/strongblog/api-gateway-node-js/)

#### 3. ¿Cómo analizar el nivel de carga de cada uno de los subsistemas en el servidor? Buscar herramientas y aprender a usarlas.
- El comando top nos ayuda a conocer los procesos de ejecución del sistema  en tiempo real y es una de las herramientas más importantes para un administrador.
- Ganglia
- Pandora FMS
- Zennix

#### 4. Buscar ejemplos de balanceadores software y hardware (productos comerciales).
## Software
- LVS
- Zevenet
- Pirhana

## Hardware
- LoadMaster LM-8020M Load Balancer
- Routers Cisco

#### Buscar productos comerciales para servidores de aplicaciones. 
-  WebLogic de Oracle
-  EAServer de Sybase Inc.
-  Wildfly versión comunitaria de JBoss Red Hat

#### Buscar productos comerciales para servidores de almacenamiento.
- Qnap TS-453A
- Windows Storage Server
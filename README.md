# Infraestructura en AWS (Amazon Web Services)
Creación de una infraestructura para alojar una plataforma Web basada en WordPress

## Introducción
*Es una versión resumida de mi trabajo final para el Ciclo Superior de ASIR (Administración de sistemas informáticos en red).*

Este proyecto busca diseñar una arquitectura segura en la nube utilizando Amazon Web Services (AWS). La infraestructura propuesta incluirá un servidor web Apache para alojar una plataforma basada en WordPress, junto con una base de datos MySQL gestionada mediante Amazon RDS (Relational Database Service). El objetivo principal de este proyecto es desarrollar una arquitectura en la nube segura, escalable y de alta disponibilidad. Para lograrlo, se implementará instancias EC2 con **balanceadores de carga** y **grupo de autoescalado** en conjunto con AWS WAF (Web Application Firewall).


## Índice
1. [Creación de la nube virtual privada (VPC) y segmentación de red.](#id1)
2. [Creación de la instancia EC2.](#id2)
3. [Configurar servidor web Apache en la instancia EC2 para alojar una plataforma desarrollada con WordPress.](#id3)
4. [Implementar una base de datos MySQL en Amazon RDS con configuraciones de replicación de datos y la creación de copias de seguridad automatizadas.](#id4)
5. [Optimizar el rendimiento de la plataforma mediante la escalabilidad automática y el balanceo de carga.](#id5)
6. [Asegurar la infraestructura utilizando AWS Shield y AWS WAF.](#id6)


<div id='id1'></div>

## Nube virtual privada y subredes

Para garantizar la máxima seguridad y privacidad de la infraestructura, el primer paso fundamental es crear una Nube privada Virtual (VPC) en AWS. Esta VPC funcionará como nuestro entorno aislado en la nube donde se despliegan todos los recursos del proyecto. 
El siguiente diagrama muestra los recursos que se planea utilizar, en el que se puede observar las redes privadas y públicas en dos zonas de disponibilidad, los grupos de seguridad y la puerta de enlace a Internet.
![alt text](/images/image.png)
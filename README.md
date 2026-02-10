Implementación de Servidor Web + Odoo
Rodriguez Solutions
Presentación del Proyecto

Este proyecto documenta la instalación y configuración de un servidor Linux destinado a alojar servicios web empresariales, incluyendo un entorno ERP Odoo accesible mediante dominio local.

El objetivo principal fue implementar una infraestructura funcional que permita:

Acceso remoto seguro

Publicación de sitio web mediante Apache

Configuración de dominio local (DNS)

Implementación del ERP Odoo 16

Arquitectura del Servidor

Servicios implementados:

Servicio	Función
SSH	Acceso remoto seguro
Apache	Servidor web
DNS local	Resolución de dominio
Odoo 16	ERP empresarial

Dominio configurado:

http://www.rodriguez.local

Acceso remoto – SSH

Permite administrar el servidor de forma segura desde otra máquina.

ssh usuario@ip_servidor


Verificación del servicio:

sudo systemctl status ssh

Servidor Web – Apache

Instalación:

sudo apt update
sudo apt install apache2 -y


Verificación:

sudo systemctl status apache2


Directorio web:

/var/www/html


Acceso desde navegador:

http://IP_SERVIDOR

Configuración DNS Local

Se configuró el dominio:

www.rodriguez.local


Archivo hosts del cliente:

192.168.1.10   www.rodriguez.local


Esto permite acceder al servidor usando nombre de dominio.

⚙️ Implementación de Odoo 16
Instalación base
sudo apt install python3-pip python3-venv git -y


Clonación del repositorio:

git clone https://www.github.com/odoo/odoo --depth 1 --branch 16.0 /opt/odoo/odoo

Entorno virtual Python

Creación del entorno:

python3 -m venv venv


Activación:

source venv/bin/activate


Instalación de dependencias:

pip install -r odoo/requirements.txt

Problemas encontrados y solución

Durante la instalación de Odoo surgieron dificultades importantes:

Problemas detectados

Conflictos con Python 3

Fallos al instalar requirements.txt

Odoo no iniciaba correctamente

Entorno virtual no activado

Solución aplicada

Activación correcta del entorno virtual

Reinstalación de dependencias

Reinicio de servicios Apache y Odoo

Tras la corrección, el sistema quedó funcional.

Resultado final del sistema

Servicios funcionando correctamente:

✔ Apache activo

✔ Dominio local resolviendo

✔ Odoo accesible desde navegador

Acceso final:

http://www.rodriguez.local

Evidencias de funcionamiento
Funcionamiento HTTP (Apache)

Insertar captura aquí

docs/img/apache_funcionando.png

Funcionamiento Odoo

Insertar captura aquí

docs/img/odoo_funcionando.png

Resolución DNS

Insertar captura aquí

docs/img/dns_funcionando.png

Descarga del Manual Completo

El manual técnico completo del proyecto se encuentra disponible en el siguiente archivo:

Manual en PDF

docs/Manual_Final_Rodriguez_Solutions.pdf

Servidor Web y ERP Odoo 16
Proyecto – Rodriguez Solutions
Índice

Objetivo del Proyecto

Arquitectura del Servidor

Acceso Remoto SSH

Servidor Web Apache

Configuración DNS

Implementación Odoo 16

Problemas y Soluciones

Evidencias

Descarga del Manual

Conclusión

Objetivo del Proyecto

Implementar un servidor Linux empresarial capaz de:

Publicar un sitio web mediante Apache

Resolver un dominio local mediante DNS

Permitir administración remota segura mediante SSH

Ejecutar el ERP Odoo 16 para uso empresarial

Dominio configurado:

http://www.rodriguez.local

Arquitectura del Servidor
Servicio	Puerto	Función
SSH	22	Acceso remoto
Apache	80	Servidor Web
DNS	53	Resolución de dominio
Odoo	8069	ERP Empresarial
Acceso Remoto SSH

Permite la administración remota del servidor sin desactivar el firewall.

Conexión al servidor
ssh usuario@IP_SERVIDOR

Verificar estado del servicio
sudo systemctl status ssh

Servidor Web Apache
Instalación
sudo apt update
sudo apt install apache2 -y

Verificación del servicio
sudo systemctl status apache2

Directorio web
/var/www/html


Acceso desde navegador:

http://IP_SERVIDOR

Configuración DNS

Se configuró un dominio local para acceder al servidor mediante nombre.

Dominio creado:

www.rodriguez.local


Configuración en cliente:

192.168.0.103   www.rodriguez.local

Implementación Odoo 16
Instalación de dependencias
sudo apt install python3-pip python3-venv git -y

Clonación del repositorio
git clone https://www.github.com/odoo/odoo --depth 1 --branch 16.0 /opt/odoo/odoo

Creación del entorno virtual
python3 -m venv venv

Activación del entorno virtual
source venv/bin/activate

Instalación de dependencias
pip install -r odoo/requirements.txt

Ejecución de Odoo
./odoo-bin

Problemas y Soluciones

Durante la implementación surgieron inconvenientes técnicos.

Problemas detectados

Conflictos con Python 3

Errores al instalar dependencias desde requirements.txt

Odoo no iniciaba correctamente

Entorno virtual no activado correctamente

Error Apache: Service Unavailable

Soluciones aplicadas

Activación correcta del entorno virtual Python

Reinstalación de dependencias

Configuración de Apache como proxy hacia Odoo

Reinicio y verificación de servicios

Resultado final:

Apache funcionando correctamente

Odoo accesible desde el dominio

DNS resolviendo correctamente

Evidencias
Funcionamiento del servidor web Apache

Ruta sugerida en el repositorio:

docs/img/apache_funcionando.png

Funcionamiento de Odoo

Ruta sugerida:

docs/img/odoo_funcionando.png

Resolución del dominio DNS

Ruta sugerida:

docs/img/dns_funcionando.png

Descarga del Manual

Manual técnico completo disponible en:

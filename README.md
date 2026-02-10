# Servidor-rodriguezFR
Todo lo instalado,  con evidencia, y capturas de cada uno de los comandos
centos-rodriguez/
# Servidor CentOS - Fabian Rodriguez

Este repositorio documenta la implementación de un servidor CentOS con los siguientes servicios:

## Servicios implementados
Información general

Este documento describe la configuración básica del servidor Linux, instalación de servicios principales y problemas encontrados durante la implementación del entorno web.

Servicios instalados:

Apache (servidor web)

Odoo (ERP)

SSH (acceso remoto)

Configuración de dominio local

Acceso al servidor (SSH)

El acceso remoto se realiza mediante SSH.

Conexión desde cliente Linux / Windows (PowerShell / Git Bash)
ssh usuario@ip_del_servidor


Ejemplo:

ssh rodriguez@192.168.1.10

Verificar estado del servicio SSH
sudo systemctl status ssh

Reiniciar SSH
sudo systemctl restart ssh

Instalación y configuración de Apache
Instalación
sudo apt update
sudo apt install apache2 -y

Verificar estado
sudo systemctl status apache2

Habilitar Apache al iniciar
sudo systemctl enable apache2

Acceso al sitio web

Abrir navegador:

http://IP_DEL_SERVIDOR


Ruta del sitio web por defecto:

/var/www/html

Ver archivos del sitio

cd /var/www/html
ls


Archivo principal:

index.html

Configuración de dominio local

Se configuró el dominio local:

http://www.rodriguez.local

Archivo hosts (cliente)

En la máquina cliente se agregó:

Linux:

sudo nano /etc/hosts


Windows:

C:\Windows\System32\drivers\etc\hosts


Agregar:

192.168.1.10   www.rodriguez.local

⚙️ Instalación de Odoo
Dependencias básicas
sudo apt install python3-pip python3-venv git -y

Crear usuario para Odoo
sudo adduser --system --home=/opt/odoo --group odoo

Descargar Odoo
sudo su - odoo
git clone https://www.github.com/odoo/odoo --depth 1 --branch 16.0 /opt/odoo/odoo

Entorno virtual Python

Se creó un entorno virtual para Odoo:

cd /opt/odoo
python3 -m venv venv


Activar entorno:

source venv/bin/activate

Instalación de dependencias
pip3 install -r odoo/requirements.txt

Problemas encontrados con Odoo

Durante la instalación se presentaron inconvenientes importantes:

Problemas con Python 3

Se detectaron conflictos entre versiones de Python y librerías requeridas por Odoo.

Problemas específicos:

Errores al instalar dependencias del archivo requirements.txt

Librerías incompatibles o faltantes

Fallos por entorno virtual no activado correctamente

Problema crítico detectado

El error principal se debía a:

No activar el entorno virtual antes de ejecutar Odoo

Dependencias no instaladas dentro del entorno

Solución aplicada

1️Activar entorno virtual:

source /opt/odoo/venv/bin/activate


2️Reinstalar dependencias:

pip install -r /opt/odoo/odoo/requirements.txt


3️Ejecutar Odoo nuevamente.

🚨 Error del servidor (Service Unavailable)

Se presentó el mensaje:

Service Unavailable
The server is temporarily unable to service your request

Posibles causas

Apache saturado o detenido

Odoo no estaba ejecutándose

Error de configuración del virtual host

Tras revisar servicios y reiniciar Apache y Odoo, el sitio quedó accesible.

Estado actual

Servicios operativos:

Apache funcionando

SSH activo

Odoo accesible desde:

http://www.rodriguez.local

Notas finales

Se recomienda:

Mantener actualizado el entorno virtual

Documentar cambios futuros

Realizar backups periódicos del servidor

Si quieres, puedo hacer la versión en README profesional con índice automático o dividirla por carpetas (docs/, apache.md, odoo.md, etc.).

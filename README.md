# Servidor Web y ERP Odoo 16  
## Proyecto – Rodriguez Solutions

---

## Índice

- Objetivo del Proyecto  
- Arquitectura del Servidor  
- Acceso Remoto SSH  
- Servidor Web Apache  
- Configuración DNS  
- Implementación Odoo 16  
- Problemas y Soluciones  
- Evidencias  
- Descarga del Manual  
- Conclusión  

---

## Objetivo del Proyecto

Implementar un servidor Linux empresarial capaz de:

- Publicar un sitio web mediante Apache
- Resolver un dominio local mediante DNS
- Permitir administración remota segura mediante SSH
- Ejecutar el ERP Odoo 16 para uso empresarial

Dominio configurado:
http://www.rodriguez.local/

---

## Arquitectura del Servidor

| Servicio | Puerto | Función |
|---|---|---|
| SSH | 22 | Acceso remoto |
| Apache | 80 | Servidor Web |
| DNS | 53 | Resolución de dominio |
| Odoo | 8069 | ERP Empresarial |

---

## Acceso Remoto SSH

Permite la administración remota del servidor sin desactivar el firewall.

### Conexión al servidor
```bash
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
```
## Configuración DNS

Se configuró un dominio local para acceder al servidor mediante nombre.

## Dominio creado:

www.rodriguez.local

```bash
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


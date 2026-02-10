# Servidor Web y ERP Odoo 16  
## Proyecto – Rodriguez Solutions
Nombre: Fabián Rodríguez
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
```
## Problemas y Soluciones
## Problemas detectados

&nbsp;Conflictos con Python 3

Errores al instalar dependencias desde requirements.txt

Odoo no iniciaba correctamente

Entorno virtual no activado correctamente

Error Apache: Service Unavailable &nbsp;

# Soluciones aplicadas

&nbsp; Activación correcta del entorno virtual Python

Reinstalación de dependencias

Configuración de Apache como proxy hacia Odoo

Reinicio y verificación de servicios &nbsp;

# Resultado final:

Apache funcionando correctamente
|<img width="886" height="600" alt="image" src="https://github.com/user-attachments/assets/6cd83642-6b63-4377-8865-852b20a629b1" />|
|<img width="938" height="431" alt="image" src="https://github.com/user-attachments/assets/6bda7f96-5f0c-41ff-b516-d52a0f04e31d" />|

Odoo accesible desde el dominio
|<img width="1857" height="1092" alt="image" src="https://github.com/user-attachments/assets/6d84a6cb-94a2-425f-aecb-cce86a595e8d" />|

DNS resolviendo correctamente
|<img width="886" height="222" alt="image" src="https://github.com/user-attachments/assets/d1bfd530-5f1b-4ba9-b3d5-888b0b0abaef" />|

## Descarga del manual:[Manual_Examen.pdf](https://github.com/user-attachments/files/25212397/Manual_Examen.pdf)
 
# Conclusion:
&nbsp; La culminación de este proyecto supuso la puesta en práctica de una infraestructura básica de servicios en un servidor Linux mediante DNS, un servidor web Apache, acceso remoto por SSH y el sistema ERP Odoo 16 en el dominio **[www.rodriguez.local](http://www.rodriguez.local)**, lo que supuesto facilitar que los recursos de servicios tuviesen acceso por un nombre de dominio y no por dirección IP como si de un entorno empresarial real se tratase. &nbsp;
&nbsp; Durante la implementación del servidor Odoo surgieron dificultades con dependencias de Python, el archivo *requirements.txt* y la activación del entorno virtual de Odoo, de forma que se pudo trabajar también en las competencias de resolución de problemas y administración de sistemas Linux. &nbsp;
Las pruebas desde equipos cliente y dispositivos móviles confirmaron que la arquitectura cliente-servidor se comportaba como se esperaba. En definitiva, el proyecto muestra lo posible que resulta desplegar y administrar diversos servicios integrados dentro de una única red &nbsp; 

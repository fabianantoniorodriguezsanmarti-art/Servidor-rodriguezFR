# Servidor-rodriguezFR
Todo lo instalado,  con evidencia, y capturas de cada uno de los comandos
centos-rodriguez/
# Servidor CentOS - Fabian Rodriguez

Este repositorio documenta la implementación de un servidor CentOS con los siguientes servicios:

## Servicios implementados

- **DNS:** Dominio local `rodriguez.local`  
  - Configuración en: `DNS/named.conf` y `DNS/rodriguez.local.zone`  
  - Evidencia: `Capturas/dns.png`  

- **Apache:** Servidor web accesible desde `www.rodriguez.local`  
  - Página de prueba: `Apache/index.html`  
  - Evidencia: `Capturas/apache.png`  

- **Odoo:** ERP accesible bajo el dominio `rodriguez.local`  
  - Configuración: `Odoo/configuracion.txt`  
  - Evidencia: `Capturas/odoo.png`  

---

## Evidencia y capturas

Se incluyen capturas de pantalla que muestran los servicios funcionando correctamente:

| Servicio | Captura |
|----------|---------|
| DNS      | ![DNS](Capturas/dns.png) |
| Apache   | ![Apache](Capturas/apache.png) |
| Odoo     | ![Odoo](Capturas/odoo.png) |

---

## Manual de Usuario

El manual PDF contiene:

- Diagrama de topología de red  
- Pasos de configuración de cada servicio  
- Cómo acceder desde cliente y dispositivo móvil  
- Seguridad y administración remota vía SSH  

**Descargar PDF:** [ManualUsuario.pdf](ManualUsuario.pdf)

---

## Enlace público del repositorio

Accede al repositorio completo con todos los archivos y evidencia aquí:  
[https://github.com/TUUSUARIO/Servidor-rodriguezFR](https://github.com/TUUSUARIO/Servidor-rodriguezFR)

---

## Notas adicionales

- Todos los servicios se han configurado en CentOS con firewall activo y administración remota vía SSH.  
- Este repositorio respalda el examen práctico y sirve como guía para replicar la configuración.

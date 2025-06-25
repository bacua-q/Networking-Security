# 🔐 Laboratorio: Palo Alto Firewall + Ubuntu Server con NGINX (VMware Workstation)

## 📘 Descripción General

Este laboratorio tiene como propósito emular un entorno de red seguro donde un servidor Ubuntu Server, ubicado en la zona **DMZ**, necesita:

- Tener **acceso a Internet** para descargar actualizaciones del sistema.
- Publicar un **servicio web seguro (HTTPS)** mediante **NGINX**.
- Estar protegido por un **Firewall Palo Alto**, el cual segmenta la red en **zonas de seguridad** (Trust, DMZ, Untrust).
- Aplicar **reglas de seguridad (Security Policies)** y **traducciones de direcciones (NAT)** para garantizar una correcta y segura comunicación.

La simulación se lleva a cabo utilizando **VMware Workstation**, donde se configuran redes internas y adaptadores para representar las diferentes zonas de red.

---

## 🧩 Topología del Laboratorio

```plaintext
               INTERNET (Untrust Zone)
                      |
                [eth1/1] Palo Alto [eth1/2]
                      |                  |
                (WAN Interface)      (DMZ Interface)
                                          |
                                    Ubuntu Server

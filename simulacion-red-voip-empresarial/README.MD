# 🖥️ Simulación de Red Empresarial con Telefonía IP en GNS3

Este laboratorio simula una red empresarial distribuida en tres sucursales virtuales interconectadas mediante routers Cisco. Cada sede cuenta con una máquina virtual que utiliza **Cisco IP Communicator** para llamadas VoIP internas, configuradas mediante **Dial Peer** y el protocolo de enrutamiento **EIGRP**.


## 📌 Objetivo

Familiarizarme con la configuración de voz sobre IP (VoIP), el protocolo de enrutamiento EIGRP y el diseño de topologías escalables dentro de un entorno de simulación completo utilizando GNS3 y VMware Workstation.

## 🧰 Tecnologías Utilizadas

- 🖧 GNS3 (Simulador de red)
- 🖥️ VMware Workstation (Virtualización de PCs)
- ☎️ Cisco IP Communicator (Softphone)
- 🔁 Cisco IOS (Routers y Switches virtuales)
- 🔄 EIGRP (Protocolo de enrutamiento dinámico)
- 📡 Dial Peer (Configuración de VoIP)

## 🧱 Topología

```plaintext
+------------------+     +------------------+     +------------------+
| Oficina Central  |     |   Sucursal A     |     |   Sucursal B     |
| IP: 192.168.10.2 |     | IP: 192.168.20.2 |     | IP: 192.168.30.2 |
| Ext: 2001        |     | Ext: 3001        |     | Ext: 4001        |
+--------+---------+     +--------+---------+     +--------+---------+
         |                          |                          |
     [Switch 1]               [Switch 2]                 [Switch 3]
         |                          |                          |
      [R1] --------------------- [R2] --------------------- [R3]
        | <---- Serial Links / EIGRP Config ----> |

# NetSec Solutions SRL

### Infraestructura de Red & Ciberseguridad Avanzada

Proyecto de infraestructura tecnológica desarrollado para **NetSec Solutions SRL**, enfocado en el diseño, implementación y documentación de una arquitectura de red **segura, escalable y de alta disponibilidad**.

La solución integra conectividad entre **Santo Domingo, Santiago y La Romana**, utilizando segmentación de red, enrutamiento dinámico, VPN, redundancia y controles de seguridad.

---

## 🌐 Arquitectura

```text
                         ┌─────────────────┐
                         │    SANTIAGO     │
                         │      HUB        │
                         │   Data Center   │
                         └────────┬────────┘
                                  │
                           DMVPN + IPSec
                         ┌────────┴────────┐
                         │                 │
                  ┌──────▼──────┐   ┌────▼────────┐
                  │   SANTO     │   │ LA ROMANA   │
                  │   DOMINGO   │   │    SPOKE    │
                  │    SPOKE    │   └─────────────┘
                  └─────────────┘
```

### Sedes

| Sede              | Rol   | Características                    |
| ----------------- | ----- | ---------------------------------- |
| **Santiago**      | Hub   | Data Center y servicios centrales  |
| **Santo Domingo** | Spoke | Distribución redundante y HSRP     |
| **La Romana**     | Spoke | Segmentación y seguridad de acceso |

---

## 🔐 Tecnologías

* **DMVPN + IPSec** — conectividad segura entre sedes
* **OSPFv2** — enrutamiento dinámico
* **VLAN / 802.1Q / VTP** — segmentación de red
* **HSRP** — alta disponibilidad
* **VLSM** — optimización del direccionamiento IP
* **AAA / FreeRADIUS** — autenticación centralizada
* **DHCP / DNS** — servicios de infraestructura
* **Postfix / Dovecot** — servicios de correo
* **DHCP Snooping / Port-Security / BPDU Guard** — seguridad de Capa 2
* **SSH + ACL** — administración segura

---

## 🖥️ Infraestructura

La arquitectura contempla infraestructura Cisco para routing y switching, junto con servidores dedicados para los servicios de red y seguridad.

### Servicios principales

```text
10.17.0.43  →  RADIUS / Servicios de autenticación
10.17.0.44  →  DHCP / DNS
```

El diseño utiliza bloques privados **10.16.0.0/16, 10.17.0.0/16 y 10.18.0.0/16** para la distribución de las redes por sede.

---

## 📂 Estructura

```text
Net-Sec-Solutions-SRL/
│
├── Configuraciones/
│   ├── Santiago/
│   ├── Santo-Domingo/
│   └── La-Romana/
│
├── Documentacion/
│
├── Propuesta/
│
└── README.md
```

---

## 🎯 Objetivos

* Diseñar una infraestructura de red corporativa segura y escalable.
* Interconectar las tres sedes mediante una WAN segura.
* Implementar segmentación mediante VLANs y VLSM.
* Garantizar disponibilidad mediante mecanismos de redundancia.
* Centralizar la autenticación y los servicios de infraestructura.
* Aplicar controles de seguridad en las capas de acceso y administración.
* Documentar la arquitectura y las configuraciones implementadas.

---

## 🏢 NetSec Solutions SRL

**Infraestructura de Red & Ciberseguridad Avanzada**

> *Seguridad, disponibilidad y conectividad para infraestructuras críticas.*

---

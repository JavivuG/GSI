# GSI — Garantía y Seguridad de la Información

Prácticas de seguridad de la información: laboratorio con máquinas virtuales, análisis de servicios de red, hashing y cifrado, certificados y firma digital, y *pentesting* de una aplicación web.

> Asignatura **Garantía y Seguridad de la Información** · 3.º curso, 1.er cuatrimestre · Curso 2023-2024 · Grado en Ingeniería Informática, Universidad de Valladolid.

## Qué hace

| Práctica | Tema | Entrega |
|----------|------|---------|
| [Práctica 1](Practica1/) | Preparación del entorno virtual: máquinas *alice*, *bob* y *mallet* en VirtualBox sobre una red NAT propia, más un esquema en Packet Tracer | [p1_GarciaGonzalez.pdf](Practica1/p1_GarciaGonzalez.pdf) |
| [Práctica 2](Practica2/) | Análisis de servicios de red: descubrimiento de equipos y puertos con Nmap (ICMP, SYN), y servicios como `telnet` y `ssh` | [p2_GarciaGonzalez.pdf](Practica2/p2_GarciaGonzalez.pdf) |
| [Práctica 3](Practica3/) | Hashing, cifrado y certificados: propiedades de las funciones hash, `md5sum`/`sha*sum`, identificación de hashes y contraseñas de `/etc/shadow` | [p3_GarciaGonzalez.pdf](Practica3/p3_GarciaGonzalez.pdf) |
| [Práctica 4](Practica4/) | Certificados y firma digital: generación y validación de firmas, y análisis del certificado de un servidor web real | [parte 1](Practica4/p4_parte1_GarciaGonzalez.pdf), [parte 2](Practica4/p4_parte2_GarciaGonzalez.pdf) |
| [Práctica 5](Practica5/) | *Pentesting* en aplicativos web: reconocimiento con Nmap y explotación de una descarga de ficheros del servidor que permite leer el código fuente | [p5_GarciaGonzalez.pdf](Practica5/p5_GarciaGonzalez.pdf) |
| [Proyecto final](Proyecto_final/) | Enunciado y materiales para la primera versión de un Sistema de Gestión de la Seguridad de la Información (SGSI) para una empresa ficticia | — |

Las entregas son informes en PDF. Las carpetas incluyen también los enunciados y la bibliografía de apoyo (capítulos de *Applied Information Security*, de Basin et al.).

## Tecnologías

- VirtualBox (máquinas virtuales y red NAT) y Cisco Packet Tracer
- Nmap, `telnet`, `ssh` y tcpdump (consulta las [referencias de la práctica 2](Practica2/links.txt))
- Utilidades de hash (`md5sum`, `sha1sum`, `sha256sum`, `sha512sum`, `hashid`)
- Criptografía de clave pública: RSA, funciones hash y certificados digitales
- Metodología MAGERIT v3 y familia ISO/IEC 27000 (proyecto SGSI)

## Aspectos técnicos destacados

- **Laboratorio aislado**: el entorno de trabajo se monta con máquinas virtuales (*alice*, *bob* y *mallet*) conectadas a una red NAT dedicada en VirtualBox. El esquema de red de la práctica 3 está en [diagrama-red-practica3.png](Practica3/diagrama-red-practica3.png).
- **Firma digital paso a paso**: el informe describe la secuencia hash → cifrado con la clave privada → verificación con la clave pública, y razona qué se pierde al prescindir de la función hash.
- **Pentesting razonado**: en la práctica 5 se parte del reconocimiento de puertos, se plantea una hipótesis sobre el endpoint de descarga y se confirma descargando ficheros PHP del *backend*.
- **Gestión del riesgo**: el proyecto final incluye las plantillas de inventario de activos, matriz y análisis de riesgos (`.xls`, `.xlsx`, `.xlsm`) y las guías de MAGERIT.

## Estructura del repositorio

```text
GSI/
├── Practica1/        # Entorno virtual (+ practica1.pkt)
├── Practica2/        # Servicios de red (Nmap)
├── Practica3/        # Hashing y cifrado (+ diagrama de red)
├── Practica4/        # Certificados y firma digital (2 partes)
├── Practica5/        # Pentesting web
└── Proyecto_final/
    ├── 2023-2024-PSGSI-Enunciado.pdf
    ├── Materiales de trabajo/                     # MAGERIT, guías SGSI y de gestión de riesgos
    └── Plantillas para realizar los cálculos/      # Hojas de cálculo de análisis de riesgos
```

## Requisitos

- Un lector de PDF para los informes y enunciados
- Cisco Packet Tracer para `Practica1/practica1.pkt`
- Para reproducir las prácticas: VirtualBox, distribuciones Linux para las máquinas virtuales (las imágenes no están en el repositorio) y Nmap

## Cómo reproducir

```bash
git clone https://github.com/JavivuG/GSI.git
cd GSI
```

El repositorio no contiene código ejecutable. Cada práctica se reproduce siguiendo su enunciado (`P*_GSI_2324*.pdf`) y el informe correspondiente, que recoge los comandos y capturas. Las máquinas virtuales se excluyen del repositorio en el `.gitignore`.

## Autoría

Javier García González.

---

Forma parte de [UVa-Projects](https://github.com/JavivuG/UVa-Projects).

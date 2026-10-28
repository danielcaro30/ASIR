# Actividad práctica NF2: gestión de la información y recursos en red

- **Asignatura:** ISO
- **Unidad / tema:** NF2 (RA3, RA4, RA5)
- **Fecha de entrega:** 2026-11-05 23:59, en **PDF**
- **Estado:** 🔄 En curso

> Aparte están las 3 actividades **teóricas** NF2 RA3, RA4 y RA5 en la plataforma (misma fecha). No van en este Word.

## Qué pide

Word con capturas en 6 bloques: particiones (Windows 11 Pro + Ubuntu 26.04 gráfico **o** consola), RAID en Windows Server, copias de seguridad con Windows Server Backup, Directorio Activo I (instalar WS2025 **en inglés**, AD + DNS, OU/usuarios/grupos, carpetas compartidas con permisos), Directorio Activo II (unir W11 al dominio, horarios/equipos de inicio, GPO, delegación) y NFS **o** SAMBA.

## Puntuación (sobre 10)

| Bloque | Puntos |
|---|---|
| 1.1 Particiones Windows 11 Pro | 1,25 |
| 1.2 Particiones Ubuntu (gráfico **o** consola) | 1,25 |
| 2 RAID | 1,25 |
| 3 Copias de seguridad | 1,25 |
| 4 AD I (WS2025 inglés 0,5 · AD 0,5 · estructura 0,5 · permisos 1) | 2,5 |
| 5 AD II (dominio 0,5 · inicio sesión 0,25 · GPO 0,5 · delegación 0,25) | 1,5 |
| 6 NFS o SAMBA | 1 |

⚠️ Windows Server instalado en **español** = −2 puntos.

## Apuntes que hacen falta

En `apuntes/` (las videoconferencias `NF2-videoconferencia-1/2/3.pdf` solo resumen y remiten a estos):

| Bloque | Apuntes (página del PDF) |
|---|---|
| 1 Particiones | `NF2-1-…informacion.pdf` · 1.9 (págs. 40-67): MBR/GPT, primaria/extendida/lógica, Administración de discos, diskpart, fdisk, herramientas de terceros |
| 2 RAID | `NF2-1-…` · 1.10-1.11 (págs. 68-78) |
| 3 Copias | `NF2-1-…` · 1.13-1.18 (págs. 79-85) |
| 4.2-4.3 AD y estructura | `NF2-2-administracion-de-dominios.pdf` · 2.3 dominio (10-23), 2.6 cuentas (29-34), 2.10 grupos (43+) |
| 4.4 Permisos carpetas | `NF2-3-administracion-del-acceso-al-dominio.pdf` · 3.2 (11-15), 3.4 (17-34), 3.6 (36-37) |
| 5.1 Unir al dominio | `NF2-3-…` · 3.1 (4-10) |
| 5.2 Horario / equipos | `NF2-2-…` · 2.6 cuentas de usuarios y equipos (29-34) |
| 5.3 GPO | `NF2-3-…` · 3.7 (38+) |
| 5.4 Delegación | `NF2-3-…` · 3.5 (35) |
| 6 NFS/SAMBA | `NF2-3-…` · 3.3 (16) |

**Falta subir** (contenido extra de la plataforma):

- [ ] **Windows Server 2025 en inglés** e **Instalación Active Directory**.
- [ ] **Discos y particiones en Linux mediante consola** (solo si Ubuntu por consola).
- [ ] **NFS.pdf** o **SAMBA.pdf** (el que elija Daniel).

## Orden de trabajo propuesto

1. Bloque 1.1 Particiones Windows 11 Pro (VM actual).
2. Bloque 1.2 Particiones Ubuntu (clon de la VM Ubuntu de NF1).
3. Bloque 4.1 Instalar Windows Server 2025 en inglés (base para RAID y copias).
4. Bloque 2 RAID (en un clon del servidor).
5. Bloque 3 Copias de seguridad (en un clon del servidor).
6. Bloques 4.2-4.4 Directorio Activo I.
7. Bloque 5 Directorio Activo II.
8. Bloque 6 NFS o SAMBA.

## Progreso

- [x] 1.1 Windows 11 Pro: Administración de discos (disco 100 GB)
- [x] 1.1 Windows 11 Pro: aplicación de terceros (MiniTool Partition Wizard Free 13.9; disco 100 GB → 55/45 GB; disco 50 GB con 3 primarias + 3 lógicas)
- [ ] 1.2 Ubuntu
- [ ] 4.1 Windows Server 2025
- [ ] 2 RAID
- [ ] 3 Copias de seguridad
- [ ] 4.2-4.4 Directorio Activo I
- [ ] 5 Directorio Activo II
- [ ] 6 NFS / SAMBA

**Último paso dado:** Bloque 1.1 terminado (Paso 15b). Siguiente: bloque 1.2 Ubuntu (falta decidir gráfico o consola).

## Decisiones pendientes

- Apellido para los nombres (`SRVTuapellido`, `Tuapellido.campus`, carpetas…).
- Ubuntu: ¿gráfico (GParted) o consola?
- Bloque 6: ¿NFS o SAMBA?
- ¿Existen ya la VM Ubuntu de NF1 y una VM Windows Server de NF1?

## Dudas y avisos

- **VM Windows 11 en NAT** (para internet). Si tenía IP fija de NF1 se quitó (DHCP). Para el bloque 5 (unirla al dominio) volver a **Host-only + IP fija**.

- **`coor1` no existe** en la estructura del dominio: el grupo Coordinación lo forman prof1 y prof2. Para las filas de «coor1 / usuario de coordinación» usar **prof2** (prof1 ya se prueba aparte). Si se prefiere, crear `coor1` y meterlo en Coordinación, pero no lo pide la estructura.
- Windows 11, parte con aplicación de terceros: 6 particiones en un disco MBR → harán falta **3 primarias + extendida con lógicas** (MBR admite máx. 4 primarias).
- RAID: se añaden 3 discos de 6 GB y 4 de 8 GB, pero el RAID 1 usa 2 y el RAID 5 usa 3: el disco que sobra es el **repuesto** para simular la sustitución.
- Bloque AD: la carpeta compartida de VMware dice «c:\Actividad UF2\…» (debería ser NF2); usar el nombre tal cual lo pide el Word.

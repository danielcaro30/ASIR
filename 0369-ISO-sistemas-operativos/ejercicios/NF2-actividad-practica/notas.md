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

En el repo solo están las diapositivas de las videoconferencias (`apuntes/NF2-videoconferencia-1/2/3.pdf`). Remiten a material que **falta subir**:

- [ ] Apuntes **NF2 1. Administración y aseguramiento de la información** (págs. 68-78 → RAID; también particiones y copias).
- [ ] Apuntes **NF2 2. Administración de dominios**.
- [ ] Apuntes **NF2 3. Administración del acceso al dominio** (3.2, 3.4, 3.6 → permisos).
- [ ] Contenido extra: **Windows Server 2025 en inglés** e **Instalación Active Directory**.
- [ ] Contenido extra: **NFS.pdf** o **SAMBA.pdf** (el que elija Daniel).

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

- [ ] 1.1 Windows 11 Pro: Administración de discos (disco 100 GB)
- [ ] 1.1 Windows 11 Pro: aplicación de terceros (disco 100 GB + disco 50 GB)
- [ ] 1.2 Ubuntu
- [ ] 4.1 Windows Server 2025
- [ ] 2 RAID
- [ ] 3 Copias de seguridad
- [ ] 4.2-4.4 Directorio Activo I
- [ ] 5 Directorio Activo II
- [ ] 6 NFS / SAMBA

**Último paso dado:** Paso 1 (instantánea + disco de 100 GB en la VM Windows 11).

## Decisiones pendientes

- Apellido para los nombres (`SRVTuapellido`, `Tuapellido.campus`, carpetas…).
- Ubuntu: ¿gráfico (GParted) o consola?
- Bloque 6: ¿NFS o SAMBA?
- ¿Existen ya la VM Ubuntu de NF1 y una VM Windows Server de NF1?

## Dudas y avisos

- **`coor1` no existe** en la estructura del dominio: el grupo Coordinación lo forman prof1 y prof2. Para las filas de «coor1 / usuario de coordinación» usar **prof2** (prof1 ya se prueba aparte). Si se prefiere, crear `coor1` y meterlo en Coordinación, pero no lo pide la estructura.
- Windows 11, parte con aplicación de terceros: 6 particiones en un disco MBR → harán falta **3 primarias + extendida con lógicas** (MBR admite máx. 4 primarias).
- RAID: se añaden 3 discos de 6 GB y 4 de 8 GB, pero el RAID 1 usa 2 y el RAID 5 usa 3: el disco que sobra es el **repuesto** para simular la sustitución.
- Bloque AD: la carpeta compartida de VMware dice «c:\Actividad UF2\…» (debería ser NF2); usar el nombre tal cual lo pide el Word.

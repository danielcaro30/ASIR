# Actividad NF1: arquitectura de sistemas

- **Asignatura:** FH
- **Unidad / tema:** NF1 (RA1)
- **Fecha de entrega:** 2026-10-20 (según el enunciado; ya pasada, pendiente de que Daniel confirme plazo)
- **Estado:** 🔄 En curso

## Qué pide

Ejercicios 9 a 13 (`enunciado.pdf`): memoria (caché, latencia, ancho de banda, dual channel), diagnóstico y benchmark del propio equipo con capturas, mirar XMP o Secure Boot/TPM en la BIOS (sin cambiar nada), diseñar un PC con presupuesto (inicial **D → 550 €**) y tabla de averías. Entrega en PDF con la respuesta debajo de cada enunciado.

## Apuntes que hacen falta

- Ej. 9 (memoria): `nf1-1.2-componentes-funcionales.pdf`, diap. 31-43 y 53 (bus de datos).
- Ej. 10 y 12 (componentes, disco, fuente): `nf1-1.2`.
- Ej. 11 (BIOS/UEFI, Secure Boot, TPM): `nf1-1.3-bios-y-gestores-de-arranque.pdf`.
- `nf1-1.1` (representación de la información): apenas se usa en esta actividad.

## Progreso

- [x] 9.1 Comando: `Get-CimInstance Win32_Processor | Select-Object Name, L2CacheSize, L3CacheSize` (Daniel dice hecho; falta que pase la captura)
- [x] 9.2 Latencia, velocidad y ancho de banda de 3 memorias
- [x] 9.3 DDR4-3600 CL18 vs DDR5-5200 CL40
- [ ] 9.4 Elegir 32 GB
- [ ] 9.5 8+8+16 GB y dual channel
- [ ] 9.6 DDR4 3200/2933/2666
- [ ] 10.1-10.6 CPU-Z/HWiNFO, CrystalDiskInfo, benchmark (capturas)
- [ ] 11.1 BIOS/UEFI (foto)
- [ ] 12 Diseña tu equipo (550 €)
- [ ] 13 Averías
- [ ] Generar el PDF de entrega

## Respuestas ya corregidas

- **9.2.1** DDR4-3600 CL18: frecuencia real 3600/2 = 1800 MHz · latencia (18/1800)×1000 = 10 ns · ancho de banda 8 B × 3600×10⁶ = 28 800×10⁶ B/s = 28 125 000 KB/s = 27 465,82 MB/s ✅ (en dual channel, ×2 = 54 931,64 MB/s)
- **9.2.2** DDR5-5200 CL40: frecuencia real 2600 MHz · latencia (40/2600)×1000 = 15,38 ns · 41 600×10⁶ B/s = 40 625 000 KB/s = 39 672,85 MB/s ✅ (dual channel ×2 = 79 345,70 MB/s). Ojo: en su línea de MB/s escribió 28.125.000 en vez de 40.625.000 (errata, resultado bien).
- **9.2.3** DDR4-2666 CL19 (1 módulo, sin dual channel): frecuencia real 1333 MHz · latencia (19/1333)×1000 = 14,25 ns · 21 328×10⁶ B/s = 20 828 125 KB/s = 20 339,97 MB/s ✅ (él puso 20 339,96: redondeo)
- **9.3** Elige DDR5-5200 CL40: ~44 % más ancho de banda (39 672,85 vs 27 465,82 MB/s) a cambio de ~5 ns más de latencia (15,38 vs 10); DDR5 = más transferencia, menos consumo (diap. 39 y 43); depende de que la placa admita DDR5 ✅

## Dudas y avisos

- El enunciado de 9.3 cita «1.2.1» y «1.2.2», pero se refiere a 9.2.1 y 9.2.2 (errata).
- 9.1: ningún apunte da un comando para ver la caché → ⚠️ el comando no sale en los apuntes.
- 9.2 pide «ancho de banda»: los apuntes solo dan la fórmula del bus (ancho del bus × frecuencia, 64 bits por canal).

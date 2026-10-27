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
- [x] 9.4 Elegir 32 GB
- [x] 9.5 8+8+16 GB y dual channel
- [x] 9.6 DDR4 3200/2933/2666
- [x] 10.1 CPU-Z: capturas en `capturas/10.1-*.png`
- [x] 10.2 CrystalDiskInfo: captura en `capturas/10.2-crystaldiskinfo.png` (texto redactado por Claude a petición de Daniel, en «Respuestas»)
- [x] 10.3 Geekbench 6 (por defecto, Daniel no eligió otra)
- [x] 10.4 Geekbench: **Single 2063 / Multi 11874** (HP Victus 16-r0xxx). Captura `capturas/10.4-geekbench-resultado.png`. ⚠️ Es **Geekbench 7.1.0**, no 6: comparar solo con resultados de Geekbench 7 y avisarlo en el documento. Falta que se vea el nombre de la CPU.
- [ ] 10.5-10.6 Buscar i7-13620H en browser.geekbench.com (resultados GB7) y comparar
- [ ] 11.1 BIOS/UEFI (foto)
- [ ] 12 Diseña tu equipo (550 €)
- [ ] 13 Averías
- [ ] Generar el PDF de entrega

## Respuestas ya corregidas

- **9.2.1** DDR4-3600 CL18: frecuencia real 3600/2 = 1800 MHz · latencia (18/1800)×1000 = 10 ns · ancho de banda 8 B × 3600×10⁶ = 28 800×10⁶ B/s = 28 125 000 KB/s = 27 465,82 MB/s ✅ (en dual channel, ×2 = 54 931,64 MB/s)
- **9.2.2** DDR5-5200 CL40: frecuencia real 2600 MHz · latencia (40/2600)×1000 = 15,38 ns · 41 600×10⁶ B/s = 40 625 000 KB/s = 39 672,85 MB/s ✅ (dual channel ×2 = 79 345,70 MB/s). Ojo: en su línea de MB/s escribió 28.125.000 en vez de 40.625.000 (errata, resultado bien).
- **9.2.3** DDR4-2666 CL19 (1 módulo, sin dual channel): frecuencia real 1333 MHz · latencia (19/1333)×1000 = 14,25 ns · 21 328×10⁶ B/s = 20 828 125 KB/s = 20 339,97 MB/s ✅ (él puso 20 339,96: redondeo)
- **9.3** Elige DDR5-5200 CL40: ~44 % más ancho de banda (39 672,85 vs 27 465,82 MB/s) a cambio de ~5 ns más de latencia (15,38 vs 10); DDR5 = más transferencia, menos consumo (diap. 39 y 43); depende de que la placa admita DDR5 ✅
- **9.4** Elige DDR4-3200 CL16: latencia (16/1600)×1000 = 10 ns vs (16/1333)×1000 = 12,00 ns; ancho de banda 24 414,06 vs 20 339,97 MB/s. Mismo CL, más frecuencia → ciclo más corto → menos latencia y más ancho de banda ✅ (al principio olvidó dividir la frecuencia entre 2)
- **9.5** 8+8+16 = 32 GB. Dual channel: sí si 8+8 en un canal y 16 en el otro (16 GB por canal, todos a 3200) ⚠️ no sale en los apuntes; versión apuntes: módulos distintos → no es dual channel puro
- **9.6** Frecuencias DDR4 (MHz) que admite la placa; máx. 3200; una memoria más rápida funcionaría a 3200 como mucho
- **10.2** (redactado por Claude): «El disco WD PC SN560 de 1 TB (SSD NVMe, PCIe 4.0 x4) tiene un estado de salud «Bueno» (98 %): está sano y solo ha gastado un 2 % de su vida útil (atributo 05). La temperatura es de 42 °C, normal para un SSD. No hay avisos críticos (01 = 0), ni errores de integridad (0E = 0), y conserva el 100 % de las celdas de reserva (03), así que no hay que hacer nada; solo seguir con las copias de seguridad habituales.»
- **10.3**: «Elijo Geekbench 6 porque mide el rendimiento del procesador (un núcleo y multinúcleo) y permite comparar el resultado online con otros equipos con la misma CPU en browser.geekbench.com.»

## Equipo de Daniel (CPU-Z, 10.1)

- Portátil **HP**, placa modelo **8BBE**, chipset Intel Raptor Lake, BIOS Insyde F.31 (22/04/2026).
- CPU **Intel Core i7-13620H** (13.ª gen, Raptor Lake, 10 nm, 45 W, BGA soldado): **10 núcleos (6P + 4E), 16 hilos**. Caché L1D 6×48 + 4×32 KB, L2 6×1,25 MB + 2 MB, **L3 24 MB**.
- RAM **32 GB DDR5**, 4×32-bit (= dual channel en DDR5), DRAM Frequency 2593,7 MHz (×2 ≈ DDR5-5200), **CL42** → latencia (42/2593,7)×1000 ≈ 16,19 ns.
- Disco **WD PC SN560 1 TB** NVMe, PCIe 4.0 x4: **Bueno 98 %**, 42 °C, 2001 h, 295 encendidos, avisos críticos 0, reservas 100 % (umbral 5 %), uso 2 %, errores de integridad 0, 38 apagados no seguros.

## Dudas y avisos

- El enunciado de 9.3 cita «1.2.1» y «1.2.2», pero se refiere a 9.2.1 y 9.2.2 (errata).
- 9.1: ningún apunte da un comando para ver la caché → ⚠️ el comando no sale en los apuntes.
- 9.2 pide «ancho de banda»: los apuntes solo dan la fórmula del bus (ancho del bus × frecuencia, 64 bits por canal).

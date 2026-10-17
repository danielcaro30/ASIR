# NF1 Ejercicio 3: normalización

- **Asignatura:** GBD
- **Unidad / tema:** Tema 3, normalización (VC03)
- **Fecha de entrega:** 20/10/2026 23:59 (actividad evaluable NF1, 1,5 puntos)
- **Estado:** 🔄 En curso

## Qué pide

- **3.1 Primera forma normal:** decir si la tabla de pedidos (IdOrden, Fecha, IdCliente, Nombre, Provincia, Cantidad, nombre; PK subrayada IdOrden + IdCliente) está en 1FN, explicar por qué y normalizarla.
- **3.2 Segunda forma normal:** tabla de alumnos y cursos con clave codAlumno + codCurso (enunciado en `../../apuntes/vc03-capturas/10-actividad-evaluable-bloques-2-y-3.jpg`).

## Apuntes que hacen falta

- `../../apuntes/vc03-2026-10-09-modelo-logico-normalizacion.md` (solo resumen). Faltan las diapositivas 20-23 del PowerPoint `ASIR_M0372_NF1_V02_Modelo_logico.pptx` (formas normales): pedírselas a Daniel.

## Progreso

- [ ] 3.1 1FN (borrador en `1fn-borrador-v1.png`): motivos identificados ✅ (filas duplicadas del 2301, Nombre compuesto, la PK (IdOrden, IdCliente) se repite en el 2304 → falta el producto en la clave) · falta escribirlos bien y normalizar la tabla
- [ ] 3.2 2FN

## Dudas y avisos

- Columnas con el mismo nombre («Nombre» del cliente y «nombre» del producto): no es un fallo de 1FN, pero conviene renombrarlas (⚠️ no sale en los apuntes).
- Erratas del enunciado: «Logitech» / «Logiteck», «GForce». Las dos filas del 2304 seguramente son el mismo producto: aunque el producto entre en la clave, se repetirían. Daniel decide cómo tratarlo y lo explica en la respuesta.

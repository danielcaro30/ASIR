# NF1 Ejercicio 3: normalización

- **Asignatura:** GBD
- **Unidad / tema:** Tema 3, normalización (VC03)
- **Fecha de entrega:** 20/10/2026 23:59 (actividad evaluable NF1, 1,5 puntos)
- **Estado:** 🔄 En curso

## Qué pide

- **3.1 Primera forma normal:** decir si la tabla de pedidos (IdOrden, Fecha, IdCliente, Nombre, Provincia, Cantidad, nombre) está en 1FN, explicar por qué y normalizarla. **La tabla NO tiene clave marcada**: lo que parece subrayado en IdOrden/IdCliente es el corrector de Word.
- **3.2 Segunda forma normal:** tabla de alumnos y cursos con clave codAlumno + codCurso (enunciado en `../../apuntes/vc03-capturas/10-actividad-evaluable-bloques-2-y-3.jpg`).

## Apuntes que hacen falta

- `../../apuntes/vc03-2026-10-09-modelo-logico-normalizacion.md` (solo resumen). Faltan las diapositivas 20-23 del PowerPoint `ASIR_M0372_NF1_V02_Modelo_logico.pptx` (formas normales): pedírselas a Daniel.

## Progreso

- [ ] 3.1 1FN: tabla normalizada en `1fn-tabla-normalizada-v1.png` (fila duplicada fuera, Nombre dividido, 2304 juntado con cantidad 4). **Corregir**: el 3er motivo es que la tabla no tiene clave (IdOrden solo se repite); Daniel tiene que elegir la clave y marcarla con (PK). Pendiente decidir si IdCliente sobra (una orden es de un solo cliente → clave (IdOrden, nombreProducto)). Tilde en «Martín» y decir qué posibilidad del 2304 se aplica.
- [ ] 3.2 2FN

## Dudas y avisos

- Columnas con el mismo nombre («Nombre» del cliente y «nombre» del producto): no es un fallo de 1FN, pero conviene renombrarlas (⚠️ no sale en los apuntes).
- Erratas del enunciado: «Logitech» / «Logiteck», «GForce». Las dos filas del 2304 seguramente son el mismo producto: aunque el producto entre en la clave, se repetirían. Daniel decide cómo tratarlo y lo explica en la respuesta.

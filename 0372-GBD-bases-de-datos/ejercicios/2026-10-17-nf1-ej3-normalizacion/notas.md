# NF1 Ejercicio 3: normalización

- **Asignatura:** GBD
- **Unidad / tema:** Tema 3, normalización (VC03)
- **Fecha de entrega:** 20/10/2026 23:59 (actividad evaluable NF1, 1,5 puntos)
- **Estado:** 🔄 En curso

## Qué pide

- **3.1 Primera forma normal:** decir si la tabla de pedidos (IdOrden, Fecha, IdCliente, Nombre, Provincia, Cantidad, nombre) está en 1FN, explicar por qué y normalizarla. **La tabla NO tiene clave marcada**: lo que parece subrayado en IdOrden/IdCliente es el corrector de Word.
- **3.2 Segunda forma normal:** tabla de alumnos y cursos con clave codAlumno + codCurso (enunciado en `../../apuntes/vc03-capturas/10-actividad-evaluable-bloques-2-y-3.jpg`).
- **3.3 Tercera forma normal:** poner un ejemplo propio que no cumpla la 3FN, explicar por qué y modificarlo para que la cumpla (`enunciado-3-3.png`).

## Apuntes que hacen falta

- `../../apuntes/vc03-2026-10-09-modelo-logico-normalizacion.md` (solo resumen). Faltan las diapositivas 20-23 del PowerPoint `ASIR_M0372_NF1_V02_Modelo_logico.pptx` (formas normales): pedírselas a Daniel.

## Progreso

- [ ] 3.1 1FN (v2 en `1fn-v2.png`): motivos ✅ (pulir redacción del 3º). Clave elegida: IdOrden(PK) sin IdCliente ✅; recomendado añadir nombreProducto a la clave (una orden puede tener varios productos). Falta: tilde en «Martín», completar la nota de la errata (juntar con cantidad 4).
- [ ] 3.2 2FN: resuelto y explicado por Claude a petición de Daniel (17/10). No está en 2FN: NombreAlumno y EmailAlumno dependen solo de codAlumno; NombreCurso, ProfesorCurso y CreditosCurso solo de codCurso. Resultado: Alumno{codAlumno(PK), nombreAlumno, emailAlumno} · Curso{codCurso(PK), nombreCurso, profesorCurso, creditosCurso} · Matricula{codAlumno(PK, FK), codCurso(PK, FK)}. Excel completo con las 6 filas en `2fn-ejercicio-3-2.xlsx` (enunciado en `enunciado-3-2.png`). Pasado al documento (`2fn-entrega-v1.png`): tablas y descripciones ✅. Retoques: «qué alumno está en qué curso» con tildes, decir a qué tabla apunta cada FK, y comprobar que el análisis (no está en 2FN + por qué) está escrito encima.
- [ ] 3.3 3FN (`3fn-entrega-v1.png`): tablas arregladas ✅. Retoques: meter «dependencia transitiva» en la frase + cadena dni → codDepartamento → nombreDepartamento + «está en 2FN»; FK `departamentoCodigo`; DNI con 8 cifras; «..» doble punto; comprobar el primer recuadro (tabla sin 3FN con nombreDepartamento).

## Dudas y avisos

- Columnas con el mismo nombre («Nombre» del cliente y «nombre» del producto): no es un fallo de 1FN, pero conviene renombrarlas (⚠️ no sale en los apuntes).
- Erratas del enunciado: «Logitech» / «Logiteck», «GForce». Las dos filas del 2304 seguramente son el mismo producto: aunque el producto entre en la clave, se repetirían. Daniel decide cómo tratarlo y lo explica en la respuesta.

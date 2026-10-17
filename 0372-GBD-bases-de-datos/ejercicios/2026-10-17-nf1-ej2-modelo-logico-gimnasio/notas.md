# NF1 Ejercicio 2: modelo lógico del gimnasio

- **Asignatura:** GBD
- **Unidad / tema:** Tema 3, modelo lógico (VC03)
- **Fecha de entrega:** 20/10/2026 23:59 (actividad evaluable NF1, 3,5 puntos)
- **Estado:** 🔄 En curso

## Qué pide

Pasar el diagrama E/R del gimnasio (`enunciado-diagrama-er.png`) a esquema relacional con PK y FK (nomenclatura `entidadCampo`, p. ej. `cicloCodigo`), explicar cómo se transforman las relaciones 1:N, N:M y 1:1 (0:1-1:1), responder 4 verdadero/falso justificados y adjuntar el esquema (`enunciado-2-preguntas.png`).

## Apuntes que hacen falta

- `../../apuntes/vc03-2026-10-09-modelo-logico-normalizacion.md` y `../../apuntes/vc03-capturas/`.

## Progreso

- [x] Paso 1: entidades → tablas con su PK
- [x] Paso 2: atributos
- [x] Paso 3: relaciones (borrador de Daniel revisado). Corregido: FK de la 1:1 en Ficha con UN y erratas arregladas. ✅ Esquema correcto.
- [ ] Explicación de los pasos (borrador en `entrega-borrador-v1.png`): 1:N ✅ · N:M falta decir PK compuesta y que fecha va en esa tabla · 1:1 Parcial–Total = N:1 según la VC03 (puso 1:N), falta decir FK en Ficha con UN
- [ ] Verdadero/falso (borrador en `entrega-borrador-v1.png`): 1, 2 y 4 ✅ · 3 sigue diciendo «la cardinalidad que tiene sesión» (es la de junto a Material)
- [x] Esquema final ✅

## Dudas y avisos

- Pregunta 4 del V/F: el enunciado dice «Un monitor dirige realiza una única ficha» (errata: sobra «dirige»). La relación de las fichas es «hecha por», no «dirige».


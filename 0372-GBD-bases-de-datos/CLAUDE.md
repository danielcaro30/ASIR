# 0372 · Gestión de bases de datos (GBD): cómo trabajar

> **Método: 🧭 Guiado paso a paso, con explicación, siguiendo solo los apuntes.**
> Daniel va definiendo detalles sobre la marcha: lo que cambie, apúntalo aquí (y en la columna «Método» del `README.md` raíz y del README de esta carpeta).

## Datos

- **Curso:** 1º
- **Profesor/a:** David Porti Pujal
- **Evaluación:** <exámenes, prácticas, porcentajes…>

## Material que da el profesor

- Clases en vídeo: el profesor resuelve ejemplos y Daniel los va haciendo a la vez.
- Ejercicios con **enunciado** del que hay que sacar el **diagrama E/R**.
- Referencia de notación: `apuntes/ejemplo-clase-er-empresa-informatica.png` (diagrama E/R hecho en clase).

## Método de trabajo

- **Modo:** 🧭 guiado paso a paso. Primero entender el enunciado y luego construir el diagrama por pasos, explicando cada uno.
- **¿Seguir los apuntes al pie de la letra?:** **Sí, solo los apuntes.** Misma notación, herramientas y forma de escribir SQL que el profesor. Si propones algo que no sale en los apuntes, avísalo con «⚠️ Esto no sale en los apuntes: lo propongo porque…» y ofrece primero la alternativa de los apuntes, si la hay.
- **Qué hago yo / qué hace Daniel:** en cada paso explico qué hay que hacer y por qué; Daniel dibuja el diagrama. Quién propone primero en cada paso (Daniel o yo): por confirmar con él.

### Pasos para sacar un diagrama E/R de un enunciado

1. **Leer** el enunciado entero sin marcar nada.
2. **Marcar** en una pasada: entidades (sustantivos con datos propios), atributos (datos sueltos), relaciones (verbos que unen dos cosas), cantidades (uno, varios, máximo 5, puede, debe…) y tipos/subtipos (jerarquías).
3. **Entidades**, cada una con su clave primaria.
4. **Relaciones** y su **cardinalidad**, con la pregunta doble («un X, ¿con cuántos Y como mínimo y como máximo?», y al revés).
5. **Atributos**: de entidad o de relación; marcar los especiales (multivaluado, derivado, clave alternativa).
6. **Jerarquías**, si las hay: disjunta o solapada, total o parcial.
7. **Dibujar** por capas: entidades, relaciones, cardinalidades, atributos.
8. **Repasar** frase a frase que todo el enunciado está en el diagrama.

⚠️ Este orden es el método habitual, no sale de los apuntes. Si el profesor lo hace de otra forma, manda la suya.

### Notación del profesor (sacada del ejemplo de clase)

- Entidad = rectángulo · relación = rombo · atributo = elipse.
- Clave primaria = subrayado continuo · clave alternativa = subrayado punteado (DNI).
- Multivaluado = elipse doble · derivado = elipse discontinua + nota con la fórmula.
- Cardinalidad `(mín:máx)` junto a cada entidad: dice cuántas de **esa** entidad van con una de la otra. Tipo (`1:N`, `N:M`, `N:1`) junto al rombo.
- Jerarquía = triángulo con `d` (disjunta); doble línea desde el supertipo = total.
- Atributos de relación colgando del rombo; si uno va subrayado (p. ej. `fechaInicio`), forma parte de la clave de la relación.

## Formato de entrega

- 

## Estilo

- **Con explicación**: explica el porqué de cada cosa para que Daniel lo entienda de cara al examen.
- En español y con formato escaneable (SQL en bloques de código).

## Qué NO hacer

- 

## Contenidos (orientativo, confirmar con los apuntes)

- Sistemas de almacenamiento y SGBD.
- Diseño conceptual (modelo entidad-relación) y modelo relacional; normalización.
- SQL: creación de tablas (DDL), consultas y manipulación de datos (DML).
- Vistas, usuarios y privilegios, transacciones.
- SGBD habitual: MySQL/MariaDB u Oracle (confirmar cuál usa el profesor).

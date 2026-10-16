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
- Material de PlanetaFP (el centro). En `apuntes/`:
  - `nf01-tema2-modelo-conceptual-diagrama-er.pdf`: teoría del tema 2 (diagrama E/R), 43 diapositivas.
  - `nf01-tema2-ejercicios-solucion.pdf`: 5 enunciados con su propuesta de solución (Microhard, Explotación minera, Chucherías, Aeropuertos, Cineasta).
  - `ejemplo-clase-er-empresa-informatica.png`: diagrama E/R hecho en clase (empresa informática).
  - `vc03-2026-10-09-modelo-logico-normalizacion.md` + `vc03-capturas/`: resumen y capturas de la VC03 (paso a tablas, normalización, evaluación del NF1).
- Herramienta de dibujo: draw.io (la usa Daniel; también sale en los apuntes).

## Método de trabajo

- **Modo:** 🧭 guiado paso a paso. Primero entender el enunciado y luego construir el diagrama por pasos, explicando cada uno.
- **¿Seguir los apuntes al pie de la letra?:** **Sí, solo los apuntes.** Misma notación, herramientas y forma de escribir SQL que el profesor. Si propones algo que no sale en los apuntes, avísalo con «⚠️ Esto no sale en los apuntes: lo propongo porque…» y ofrece primero la alternativa de los apuntes, si la hay.
- **Qué hago yo / qué hace Daniel:** en cada paso explico qué hay que hacer y por qué; Daniel dibuja el diagrama. **Daniel intenta cada paso primero** y yo lo corrijo explicando **el porqué** de cada acierto y cada fallo (el E/R es nuevo para él: quiere entenderlo, no solo tenerlo bien). Después Daniel lo dibuja.

### Pasos para sacar un diagrama E/R (los del profesor, diapositiva «Pasos para el diseño ER»)

1. **Encontrar las entidades**: objetos con existencia propia; distinguirlas de los atributos.
2. **Identificar los atributos** de entidades y relaciones (simples, compuestos, multivaluados, derivados).
3. **Buscar identificadores** (claves primarias).
4. **Especificar relaciones y cardinalidades**.

Trucos que funcionan con Daniel: leer el enunciado entero antes de marcar; para cada relación, la pregunta doble; al final, repasar frase a frase que todo el enunciado está en el diagrama.

### Notación del profesor (confirmada con los apuntes y las soluciones)

- Entidad = rectángulo · relación = rombo · atributo = elipse. Notación Chen.
- Clave primaria = subrayado continuo · clave alternativa (candidata no elegida) = subrayado punteado.
- Multivaluado = elipse doble · derivado = elipse discontinua (en clase, con nota y fórmula).
- **Cardinalidad** `(mín:máx)` (a veces con coma) junto a cada entidad: dice cuántas de **esa** entidad van con una de la otra. Diapositiva «Cardinalidad: más ejemplos»: «(1,1) al lado de Director indica que un Instituto debe tener mínimo 1 director y como mucho uno». Un máximo numérico (p. ej. 35, 3, 5) cuenta como N para el tipo.
- **Tipo** junto al rombo: `1:1`, `1:N` o `N:1` (lo mismo, según el orden de lectura), `N:M`.
- **Ternarias** (sí están en los apuntes): tipo de tres partes junto al rombo (`N:M:P`, `N:M:1`, `N:1:1` o `1:1:1`). En sus soluciones (Chucherías) **no pone (mín:máx)** en las ternarias: solo una letra (N, M, P) en cada pata.
- **Atributos de relación** colgando del rombo. Patrón en todas sus soluciones: la **fecha** de una relación va **subrayada** (forma parte de la clave) cuando la misma combinación se puede repetir en fechas distintas (atiende, repara, contrata, aterrizar, incidencia, compra).
- Nombres de relación: un verbo; usa tanto conjugado (tiene, contrata, dispone) como infinitivo (Aterrizar). Los dos valen.
- Reflexivas: línea que sale y vuelve a la misma entidad.
- Débil: rectángulo doble + rombo doble; su clave parcial con subrayado discontinuo.
- Relación exclusiva: arco que cruza las líneas desde la entidad.
- Jerarquía: triángulo con `d` (disjunta) u `o` (solapada); doble línea del supertipo al triángulo = total, línea simple = parcial. Los subtipos no llevan clave (heredan la del supertipo).
- A veces dibuja doble línea entre entidad y rombo en relaciones, pero no de forma constante: no se la exijas a Daniel.

## Formato de entrega

- Diagramas E/R hechos en draw.io.
- Actividad evaluable NF1 (MWC = ejercicio 1, gimnasio = ejercicio 2, normalización = ejercicio 3): documento del enunciado con respuestas en **PDF** `ASIR_MP0372_NF1_Apellido1_Nombre.pdf` + **vídeo de ~5 min** sobre el diagrama E/R. Límite **20/10/2026 23:59**. No se entrega el archivo de draw.io.

## Estilo

- **Con explicación**: explica el porqué de cada cosa para que Daniel lo entienda de cara al examen.
- En español y con formato escaneable (SQL en bloques de código).

## Qué NO hacer

- **Actividades evaluables: el enunciado dice «Uso de IA comporta un 0 en la EC del núcleo formativo».** No resuelvas, no corrijas ni redactes partes de una actividad evaluable (diagramas, esquemas, respuestas, guion del vídeo). Si Daniel lo pide, recuérdaselo. Sí puedes explicar la teoría con ejemplos que no se evalúan (los de clase o los ejercicios ya resueltos).
- No enseñar la propuesta de solución de un ejercicio antes de que Daniel lo intente: el propio profesor pide hacerlo «sin mirar la propuesta de solución». Úsalas solo para corregir y para confirmar la notación.

## Contenidos (orientativo, confirmar con los apuntes)

- Sistemas de almacenamiento y SGBD.
- Diseño conceptual (modelo entidad-relación) y modelo relacional; normalización.
- SQL: creación de tablas (DDL), consultas y manipulación de datos (DML).
- Vistas, usuarios y privilegios, transacciones.
- SGBD habitual: MySQL/MariaDB u Oracle (confirmar cuál usa el profesor).

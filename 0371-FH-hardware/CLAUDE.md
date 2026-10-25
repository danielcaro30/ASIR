# 0371 · Fundamentos de hardware (FH): cómo trabajar

> **Método: 🧑‍🏫 Explico → Daniel lo hace → yo corrijo. Si Daniel pide que lo haga yo, lo hago (✅ resolución explicada). Solo los apuntes.**
> Daniel parte de cero en la asignatura. Si cambia de opinión, actualiza este archivo y la columna «Método» del `README.md` raíz y del README de esta carpeta.

## Datos

- **Curso:** 1º
- **Profesor/a:** Marina Iriarte Fuster
- **Evaluación:** <exámenes, prácticas, porcentajes…>

## Material que da el profesor

- Material de PlanetaFP. Actividades por núcleo formativo (NF) en PDF con recuadros para responder.
- En `apuntes/` (NF1. Arquitectura de sistemas):
  - `nf1-1.1-representacion-informacion-y-arquitecturas.pdf`
  - `nf1-1.2-componentes-funcionales.pdf`: CPU, memoria (caché, RAM, latencia, dual channel), buses, placa base, disco, fuente. 117 diapositivas.
  - `nf1-1.3-bios-y-gestores-de-arranque.pdf`

## Método de trabajo

- **Modo:** para cada apartado:
  1. **Explico** lo justo para hacerlo, sacado de los apuntes (citando la diapositiva si ayuda).
  2. **Daniel lo hace** (cálculo, respuesta, captura…).
  3. **Corrijo:** ✅ si está bien; si no, digo exactamente qué falla y por qué.
  - Si Daniel pide «hazlo tú», lo resuelvo entero y explico cada parte.
- **¿Seguir los apuntes al pie de la letra?:** **Sí, solo los apuntes.** Mismas fórmulas, unidades y conceptos. Si algo no sale en ellos (un comando, una herramienta, un dato de Internet), avísalo con «⚠️ Esto no sale en los apuntes: lo propongo porque…» y ofrece primero la alternativa de los apuntes, si la hay.
- Un apartado cada vez: no avances hasta que Daniel lo haya hecho o diga «hecho».

### Fórmulas de los apuntes (NF1.2)

- **Latencia real (ns)** = (CL / frecuencia real) × 1000, con **frecuencia real = frecuencia (MHz) / 2** (diap. 43; ejemplo DDR4-3600 CL18 = 10 ns, DDR5-5200 CL40 ≈ 15,3 ns).
- **Velocidad de transmisión** = ancho del bus × frecuencia (diap. 53). Bus de datos de **64 bits (8 bytes) por canal**. Pasos a KB/s y MB/s dividiendo entre 1024.
- **Dual channel** (diap. 41): dos módulos en paralelo, duplica el ancho de banda; módulos distintos → trabaja con las características del peor.

## Formato de entrega

- **PDF** con la respuesta **debajo de cada enunciado**, en el campus virtual.
- **Lo genero yo**: preparo el documento con las respuestas y Daniel añade las capturas (o me las pasa y las pongo yo).

## Estilo

- **Corto y directo**, en español y escaneable. Las explicaciones, breves y al grano (Daniel empieza de cero, pero no quiere teoría de relleno).
- Cálculos con todos los pasos y unidades.

## Qué NO hacer

- No dar la solución antes de que Daniel lo intente, salvo que la pida.
- No inventar métodos o fórmulas que no salgan en los apuntes sin el aviso ⚠️.
- En BIOS/UEFI: que Daniel **no cambie nada**, solo mirar y fotografiar.

## Contenidos (orientativo, confirmar con los apuntes)

- Componentes del equipo: placa base, CPU, memoria, almacenamiento, fuente.
- Montaje, mantenimiento y diagnóstico de equipos y periféricos.
- Instalación de software, imágenes y clonado.
- Centros de proceso de datos (CPD) y presupuestos.
- Prevención de riesgos y tratamiento de residuos.

# Diagrama E/R: Mobile World Congress

- **Asignatura:** GBD
- **Unidad / tema:** Modelo entidad-relación
- **Fecha de entrega:** 20/10/2026 23:59 (es el ejercicio 1 de la actividad evaluable NF1)
- **Estado:** ✅ Terminado (falta entregar)

## Qué pide

Dibujar el diagrama E/R del enunciado (`enunciado.md`): compañías, representantes, dispositivos, stands, salas, eventos, periodistas y patrocinadores del Mobile World Congress.

## Apuntes que hacen falta

- `../../apuntes/nf01-tema2-modelo-conceptual-diagrama-er.pdf` (teoría; ternarias en «Relaciones Ternarias»).
- `../../apuntes/nf01-tema2-ejercicios-solucion.pdf` (soluciones de otros ejercicios; el MWC no está).
- `../../apuntes/ejemplo-clase-er-empresa-informatica.png`.

## Progreso

Vamos por capas: Daniel intenta cada paso, Claude corrige explicando el porqué y Daniel lo dibuja.

- [x] Paso 1: entidades. Daniel sacó 10 candidatas; quedan 8: Compañía, Representante, Dispositivo, Stand, Sala, Evento, Periodista, Patrocinador («productos» = Dispositivo; «presentador» será atributo). Falta que las dibuje.
- [x] Borrador v1 (`borrador-v1.webp`): 8 entidades y todos sus atributos dibujados. Correcciones pendientes:
  - Claves con subrayado punteado → continuo (punteado = clave alternativa).
  - Periodista: quitar subrayado de nombre y apellido.
  - fecha y presentador: quitar de Evento y colgarlos del rombo.
  - Rombo «presentan» → «realizar», y unirlo también a Compañía (relación ternaria Compañía–Sala–Evento).
  - Detalles: «Representate» → «Representante»; «fecha» de Dispositivo → «fechaLanzamiento»; nota de edad → «edad = fechaActual − fechaNacimiento».
- [x] Borrador v2 (`borrador-v2-parcial.png`, captura parcial): claves con subrayado continuo, ternaria Compañía–Sala–Evento con fecha y presentador en el rombo. Rombo renombrado a «realizar». Daniel pidió repetir por qué fecha y presentador van en el rombo (explicado con la tabla de realizaciones y el ejemplo de la nota de un examen). No se ven en la captura Periodista, Representante ni Dispositivo.
- [x] Paso 2: relaciones (`borrador-v3.webp`). Daniel sacó las 5 que faltaban, todas bien: pertenece (Representante–Compañía), presenta (Dispositivo–Compañía), ubicado (Stand–Compañía), patrocina (Patrocinador–Evento), asiste (Periodista–Evento). Claves ya con subrayado continuo; Periodista sin subrayados de más.
- [x] Borrador v4 (`borrador-v4.webp`): importe en patrocinar, Representante, fechaLanzamiento, nota de edad y rombos en infinitivo. Entidades, atributos y relaciones ✅ completos.
- [x] Paso 3: cardinalidades y tipo de cada relación. Ejemplo hecho por Claude: pertenecer = Representante (1:N), Compañía (1:1), tipo 1:N. Daniel hace: presentar, ubicar, patrocinar, asistir. La ternaria realizar, al final y explicada aparte. Daniel pidió repasar los tipos (1:1, 1:N, N:M): explicados con la pregunta rápida de «¿muchos a cada lado?»; le toca decir primero solo el tipo de las 4.
  - Tipos en `borrador-v5.webp`: pertenecer N:1 ✅, presentar N:1 ✅, patrocinar N:M ✅, asistir N:M ✅, ubicar N:1 ❌ (es N:M: una compañía varios stands y un stand varias compañías), realizar N:M ❌ (ternaria: N:M:P, explicado fijando dos entidades y preguntando por la tercera).
  - Siguiente: (mín:máx) de presentar, ubicar, patrocinar y asistir; luego los de la ternaria.
  - Cardinalidades en `borrador-v6.webp`: pertenecer, presentar y patrocinar ✅; ubicar N:M ✅ pero junto a Compañía puso 1:1 (debe ser (1:N)); asistir: junto a Periodista debe ser (1:50), no 1:N. Faltan paréntesis en todas las (mín:máx). realizar: falta una letra en cada pata (N, M, P) y subrayar fecha.
- [ ] Paso 4: atributos (de entidad y de relación)
- [x] Borrador v7 (`borrador-v7.webp`): todo correcto. Solo falta poner entre paréntesis las (mín:máx) junto a las entidades.
- [x] Paso 5: repaso frase a frase del enunciado: todo está en el diagrama.
- [x] Versión final `borrador-v8-final.webp`: paréntesis puestos y posiciones reorganizadas. Solo queda ensanchar la caja de «(1:50)», que corta el paréntesis.
- [ ] Entregar: diagrama + **vídeo de ~5 min** explicando el proceso y justificando decisiones. Guion hecho: `guion-video.md`. Falta grabarlo.

## Dudas y avisos

- ⚠️ Visto en la grabación de la VC03: el enunciado de la actividad evaluable dice «Uso de IA comporta un 0 en la EC del núcleo formativo». Avisado a Daniel el 16/10/2026. Daniel aclara que el profesor permite usar la IA para aprender y corregir, no para que haga los ejercicios.

- Confirmado con los apuntes: en «realizar» la fecha va **subrayada** (patrón de todas las soluciones del profesor) y la ternaria se marca con tipo N:M:P y una letra en cada pata, sin (mín:máx).

- La fecha de entrega y la herramienta de dibujo están por confirmar.

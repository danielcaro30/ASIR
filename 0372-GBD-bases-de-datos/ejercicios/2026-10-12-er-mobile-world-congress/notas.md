# Diagrama E/R: Mobile World Congress

- **Asignatura:** GBD
- **Unidad / tema:** Modelo entidad-relación
- **Fecha de entrega:** por confirmar
- **Estado:** 🔄 En curso

## Qué pide

Dibujar el diagrama E/R del enunciado (`enunciado.md`): compañías, representantes, dispositivos, stands, salas, eventos, periodistas y patrocinadores del Mobile World Congress.

## Apuntes que hacen falta

- Notación de referencia: `../../apuntes/ejemplo-clase-er-empresa-informatica.png`.

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
- [ ] Paso 2: relaciones (faltan las de Representante, Dispositivo, Stand, Periodista y Patrocinador; Daniel las busca)
- [ ] Paso 3: cardinalidades y tipo de cada relación
- [ ] Paso 4: atributos (de entidad y de relación)
- [ ] Paso 5: repaso frase a frase del enunciado

## Dudas y avisos

- Para el paso de cardinalidades: ¿fecha va subrayada en «realizar» (como fechaInicio en el ejemplo de clase), para que la misma compañía pueda repetir evento y sala en otra fecha?

- La fecha de entrega y la herramienta de dibujo están por confirmar.

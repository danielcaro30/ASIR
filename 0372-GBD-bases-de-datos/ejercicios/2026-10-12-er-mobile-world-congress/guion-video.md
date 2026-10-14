# Guion del vídeo: diagrama E/R del Mobile World Congress (~5 min)

Entrega: vídeo de unos 5 minutos explicando el proceso seguido para diseñar el diagrama E/R y justificando las decisiones.

Graba la pantalla con el diagrama abierto en draw.io y ve señalando con el ratón cada parte mientras la explicas. Cuéntalo con tus palabras: las frases de abajo son orientativas.

## 0:00 – 0:20 · Presentación

- Qué es: el diagrama E/R de la base de datos del Mobile World Congress.
- Cómo lo he hecho: con draw.io, en notación Chen, siguiendo los 4 pasos del tema: entidades, atributos, claves, y relaciones con cardinalidades.

## 0:20 – 1:20 · Paso 1: entidades

- Criterio: es entidad si el enunciado pide guardar **varios datos** de ello, hay **muchos** y algo lo **identifica**.
- Las 8 entidades: Compañía, Representante, Dispositivo, Stand, Sala, Evento, Periodista y Patrocinador.
- Lo que descarté y por qué:
  - **Productos**: es lo mismo que dispositivos (sinónimo); hago una sola entidad, la que tiene los datos.
  - **Presentador**: solo se pide saber quién presenta, sin más datos ni clave → es un **atributo**.
  - **Mobile World Congress / Barcelona / la organización**: solo hay uno, es el contexto.

## 1:20 – 2:00 · Paso 2: atributos

- Cada entidad con los datos que pide el enunciado (señálalos rápido).
- **edad** es un **atributo derivado** (elipse discontinua): se calcula con la fecha de nacimiento; lo indico con una nota: edad = fechaActual − fechaNacimiento.
- Llamé **fechaLanzamiento** a la fecha del dispositivo para no confundirla con la fecha del evento.

## 2:00 – 2:30 · Paso 3: claves primarias (subrayadas)

- Las saqué de frases como «que es único», «identificado por», «los identificamos por».
- Pasaporte en Representante y Periodista; nombre en Compañía, Dispositivo, Sala y Patrocinador; númeroStand en Stand.
- **Evento**: el enunciado no dice que el nombre sea único, pero en los ejemplos el evento se identifica solo por su nombre («el evento Presentación») y lo hacen varias compañías, así que el nombre lo identifica.

## 2:30 – 4:30 · Paso 4: relaciones y cardinalidades

Cómo se leen: el (mín:máx) junto a una entidad dice cuántas de esa entidad van con **una** de la otra; el tipo (1:N, N:M) junto al rombo sale de los máximos.

- **pertenecer** (Representante–Compañía), N:1: una compañía envía «como mínimo un representante, pero puede enviar más» → (1:N); un representante «siempre pertenece» a una y tiene «exclusividad» → (1:1).
- **presentar** (Dispositivo–Compañía), N:1: «promocionar **sus** dispositivos» → cada dispositivo es de una compañía (1:1); cada compañía presenta uno o varios (1:N).
- **ubicar** (Stand–Compañía), N:M: una compañía «puede utilizar más de un stand» y «todas deben estar en alguno» → (1:N); un stand lo pueden usar varias compañías y «todos están siendo usados» → (1:N).
- **patrocinar** (Patrocinador–Evento), N:M: «cada empresa patrocina como mínimo un evento» y «cada evento tiene como mínimo un patrocinador» → (1:N) y (1:N).
  - **importe** va en la relación: Coca-Cola da 50.000 € a I+D y 20.000 € a Presentación; no es de la empresa ni del evento, sino de la pareja.
- **asistir** (Periodista–Evento), N:M: a un evento asisten «mínimo 1 y máximo 50» periodistas → (1:50); un periodista puede ir a varios eventos → (1:N). El 50 cuenta como «muchos» para el tipo.
- **realizar** (Compañía–Sala–Evento), **ternaria N:M:P** (la decisión más importante):
  - El enunciado pide saber la fecha del evento «de una compañía en concreto, en qué sala y qué presentador»: un solo hecho junta tres entidades. Con dos relaciones binarias se perdería qué compañía hizo qué evento en qué sala.
  - N:M:P: fijando dos, la tercera puede ser muchas (Samsung + Magma → varios eventos; Magma + Presentación → Samsung y Xiaomi; Samsung + Presentación → varias salas). Pongo una letra en cada pata, como en los ejemplos del tema.
  - **fecha y presentador** cuelgan del rombo: Presentación tiene fechas y presentadores distintos según la compañía, así que no son del evento sino de cada realización.
  - **fecha va subrayada** porque forma parte de la clave: la misma compañía puede repetir el mismo evento en la misma sala otro día.

## 4:30 – 5:00 · Repaso y cierre

- Al final repasé el enunciado frase a frase para comprobar que todo está en el diagrama.
- Supuestos que tomé donde el enunciado no lo dice: cada compañía presenta al menos un dispositivo; el nombre identifica al evento; un periodista registrado ha asistido al menos a un evento.

# Instrucciones para Claude: repositorio ASIR de Daniel

Daniel estudia el **Grado Superior de ASIR** (Administración de Sistemas Informáticos en Red). Este repositorio organiza sus ejercicios **por asignatura**, y **cada asignatura se trabaja de forma distinta**. El método de cada una está en el `CLAUDE.md` de su carpeta y manda sobre cualquier costumbre general.

## 1. Identifica la asignatura antes de nada

- Pistas: lo que diga Daniel, la cabecera de los apuntes o del Word (p. ej. «0369. Implantación de sistemas operativos»), el código, el nombre del docente o el tema.
- En la plataforma del centro (grupo **PFP 2609**, 1º ASIR) los cursos se llaman `2609_ASIR_<código>_1A_O_<nombre>_C`, p. ej. `2609_ASIR_0369_1A_O_Implantación de sistemas operativos_C`. Ese código identifica la asignatura.
- Lee **siempre** el `CLAUDE.md` de esa carpeta antes de proponer nada y aplica **solo** ese método. **No mezcles métodos** entre asignaturas.
- Si no está claro de qué asignatura es, pregunta en una línea.

| Código | Siglas | Asignatura | Docente | Carpeta |
|---|---|---|---|---|
| 0369 | ISO | Implantación de sistemas operativos | Xavier Castejón Domenech | `0369-ISO-sistemas-operativos/` |
| 0371 | FH | Fundamentos de hardware | Marina Iriarte Fuster | `0371-FH-hardware/` |
| 0372 | GBD | Gestión de bases de datos | David Porti Pujal | `0372-GBD-bases-de-datos/` |
| 1709 | IPE I | Itinerario personal para la empleabilidad I | Yolanda Serrano Moyano | `1709-IPE1-empleabilidad/` |

El método actual de cada una está en la tabla del `README.md` raíz.

## 2. Si la asignatura tiene el método «POR DEFINIR»

No empieces el ejercicio con un método inventado. Antes, pregunta a Daniel (breve, en una sola tanda):

1. **Modo de trabajo** (puede combinar varios):
   - 🧭 **Guiado paso a paso**: yo doy un paso, Daniel lo hace y manda captura o «hecho», yo reviso y sigo.
   - 🧑‍🏫 **Tutor**: pistas y preguntas para que lo resuelva él; la solución solo si la pide.
   - ✅ **Resolución explicada**: resuelvo el ejercicio entero y explico cada parte.
   - 🔍 **Corrector**: Daniel lo hace y yo reviso, señalo fallos y propongo mejoras.
   - 📚 **Estudio**: resúmenes, esquemas, preguntas tipo test y simulacros de examen.
2. **Material y entrega**: qué da el profesor (PDF, Word, plataforma…) y cómo se entrega (Word con capturas, PDF, código, archivo `.pkt`…).
3. **¿Seguir los apuntes al pie de la letra** o vale usar otros métodos?
4. **Estilo**: corto y directo, o con explicación teórica.

Con sus respuestas: rellena el `CLAUDE.md` de la asignatura (quitando el aviso «POR DEFINIR»), actualiza la columna «Método» del `README.md` raíz y el del README de la asignatura, y haz commit. Después empieza el ejercicio.

Si Daniel cambia de opinión sobre cómo trabajar una asignatura, actualiza su `CLAUDE.md` en ese momento.

## 3. Dónde va cada cosa

```
<asignatura>/
├── CLAUDE.md            método de trabajo (para Claude)
├── README.md            índice y estado de los ejercicios (para Daniel)
├── apuntes/             PDFs y material del profesor
└── ejercicios/
    └── UT02-usuarios-y-grupos/
        ├── enunciado.docx       lo que da el profesor
        ├── entrega.docx         lo que se entrega
        └── notas.md             resumen, progreso y dudas
```

- Plantillas: `_plantillas/asignatura/` y `_plantillas/ejercicio/notas.md`.
- Nombres de carpetas y archivos en minúsculas, sin tildes ni espacios, con guiones. Prefijo de unidad (`UT01`, `UT02`…) si el profesor numera así; si no, la fecha `AAAA-MM-DD`.
- **Asignatura nueva** (p. ej. al pasar a 2º): copia `_plantillas/asignatura/` a `CODIGO-SIGLAS-nombre/`, rellena los datos, déjala «POR DEFINIR» y añádela a la tabla de arriba y a la del `README.md`.

## 4. Continuidad entre sesiones

Cada sesión empieza sin memoria: **el repositorio es la memoria**.

- Al empezar un ejercicio, crea su carpeta y su `notas.md` a partir de la plantilla.
- Al retomar un ejercicio, lee primero su `notas.md`.
- Si Daniel dice que ha subido algo a GitHub (apuntes, enunciados), haz `git pull` antes de buscarlo. Lo que mande como captura en el chat, guárdalo en la carpeta que toque.
- Al pausar o terminar: actualiza `notas.md` (dónde nos quedamos y qué falta), la tabla de ejercicios del README de la asignatura, y haz commit y push.

## 5. Reglas comunes

- Siempre en **español**.
- Si el método de la asignatura no dice nada del estilo: directo, escaneable y sin relleno.
- No borres ni sobrescribas apuntes ni entregas de Daniel sin preguntar.
- **Si el enunciado de una actividad prohíbe o penaliza el uso de IA, avisa a Daniel en cuanto lo veas** y no le hagas esa actividad (ni la corrijas ni redactes partes); como mucho, explica la teoría con ejemplos que no se evalúan.
- Commits en español, cortos, con las siglas delante (p. ej. «ISO: notas práctica usuarios y grupos»).

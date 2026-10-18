# ASIR: ejercicios y prácticas

Ejercicios del Grado Superior de **Administración de Sistemas Informáticos en Red**, organizados por asignatura. Cada asignatura tiene su propia forma de trabajar, definida en el `CLAUDE.md` de su carpeta.

## Asignaturas

1º ASIR · grupo PFP 2609

| Código | Siglas | Asignatura | Docente | Método de trabajo |
|---|---|---|---|---|
| 0369 | ISO | [Implantación de sistemas operativos](0369-ISO-sistemas-operativos/) | Xavier Castejón Domenech | 🧭 Guiado paso a paso en la VM, siguiendo los apuntes y con capturas |
| 0371 | FH | [Fundamentos de hardware](0371-FH-hardware/) | Marina Iriarte Fuster | ⏳ Por definir |
| 0372 | GBD | [Gestión de bases de datos](0372-GBD-bases-de-datos/) | David Porti Pujal | 🧭 Guiado paso a paso, con explicación, siguiendo solo los apuntes |
| 1709 | IPE I | [Itinerario personal para la empleabilidad I](1709-IPE1-empleabilidad/) | Yolanda Serrano Moyano | ✅ Resolución explicada, corta y directa |

La primera vez que trabajemos una asignatura «por definir», te preguntaré cómo quieres llevarla y lo dejaré apuntado en su carpeta.

## Cómo empezar un ejercicio

1. Dime la asignatura y el ejercicio (p. ej. «ISO, práctica de usuarios y grupos»).
2. Pásame el enunciado y los apuntes: adjúntalos en el chat o súbelos a la carpeta `apuntes/` o `ejercicios/` de la asignatura.
3. Leo el método de esa asignatura y trabajamos así.

Para retomar algo a medias: «seguimos con ISO usuarios y grupos». Leo su `notas.md` y continúo donde lo dejamos.

## Cómo pasarme apuntes

**Recomendado: subirlos a GitHub.** Se quedan guardados en su asignatura y los encuentro en cualquier sesión, aunque sea otro día.

1. Desde el ordenador, entra en [github.com/danielcaro30/ASIR](https://github.com/danielcaro30/ASIR).
2. Abre la carpeta de la asignatura y dentro `apuntes/`.
3. **Add file → Upload files** y arrastra los PDF (máximo 25 MB cada uno).
4. Abajo, **Commit changes**.
5. Dime «he subido apuntes de GBD» (o la asignatura que sea) y los leo.

Con el nombre que traigan vale; si hace falta, los renombro yo con el prefijo de unidad (`UT01-…`).

**Para algo puntual** (una diapositiva, una página): captura o foto en el chat. La guardo yo en `apuntes/`.

No puedo entrar en la plataforma del centro ni ver los vídeos de clase. Si algo solo sale en el vídeo, mándame una captura o cuéntamelo.

## Modos de trabajo disponibles

Cada asignatura puede usar uno o combinar varios:

| Modo | Qué hago yo | Qué haces tú |
|---|---|---|
| 🧭 Guiado paso a paso | Te doy un paso, espero tu «hecho» o captura y la reviso | Lo haces en la VM o el equipo |
| 🧑‍🏫 Tutor | Pistas y preguntas; la solución solo si la pides | Lo resuelves tú |
| ✅ Resolución explicada | Resuelvo el ejercicio entero y explico cada parte | Lo entiendes y lo entregas |
| 🔍 Corrector | Reviso lo que has hecho y te digo qué cambiar | Haces el ejercicio y me lo pasas |
| 📚 Estudio | Resúmenes, esquemas, tests y simulacros de examen | Estudias y respondes |

Para cambiar cómo se trabaja una asignatura, dímelo («en GBD prefiero que me corrijas») y actualizo su `CLAUDE.md`.

## Estructura

```
ASIR/
├── CLAUDE.md                      reglas generales para Claude
├── README.md                      este índice
├── _plantillas/                   plantillas de asignatura y de ejercicio
├── 0369-ISO-sistemas-operativos/
│   ├── CLAUDE.md                  cómo se trabaja esta asignatura
│   ├── README.md                  lista de ejercicios y su estado
│   ├── apuntes/                   PDFs del profesor
│   └── ejercicios/
│       └── UT02-usuarios-y-grupos/
│           ├── enunciado.docx
│           ├── entrega.docx
│           └── notas.md           resumen, progreso y dudas
└── …una carpeta igual por asignatura
```

## Añadir asignaturas

Dime cuál y la creo a partir de `_plantillas/asignatura/`. Las otras de 1º de ASIR son 0370 Planificación y administración de redes (PAR) y 0373 Lenguajes de marcas y sistemas de gestión de información (LMSGI). Las de 2º suelen ser 0374 Administración de sistemas operativos (ASO), 0375 Servicios de red e Internet (SRI), 0376 Implantación de aplicaciones web (IAW), 0377 Administración de sistemas gestores de bases de datos (ASGBD) y 0378 Seguridad y alta disponibilidad (SAD).

# VC03 (9/10/2026): modelo lógico y normalización

Resumen de la grabación de la videoconferencia del profesor David Porti (76 min). El vídeo no está en el repositorio porque pesa demasiado; las capturas clave están en `vc03-capturas/`. Pendiente: transcripción del audio.

## Contenido de la clase

1. **Paso del diagrama E/R al esquema relacional** (modelo lógico).
2. Ejercicio práctico: pasar a tablas el diagrama de la empresa informática (el de `ejemplo-clase-er-empresa-informatica.png`).
3. **Normalización**: 1FN, 2FN y 3FN con la tabla PRESTAMO.
4. Evaluación continua del NF1 y próxima clase.

## Reglas de transformación E/R → relacional (capturas 01, 03, 04)

- **Entidad** → una tabla.
- **Atributo** → columna de su tabla. **Clave** → (PK).
- **Atributo calculado** (derivado) → no aparece en el modelo.
- **Atributo multivalor** → tabla nueva con el atributo + la PK de la entidad como (PK, FK).
- Notación: `Cliente:{id(PK), DNI(UN), nombre, ...}`. PK = clave primaria, FK = clave foránea, UN = única (clave alternativa).

### Relaciones según cardinalidad

| Tipo | Qué se hace |
|---|---|
| **1:N** | La PK del lado 1 viaja como FK al lado N. No se crea tabla. Los atributos de la relación van con la FK. |
| **1:1** | La FK va en cualquiera de las dos tablas + UN. Mejor en el lado con participación obligatoria (1,1). Si las dos son (1,1), se puede fusionar en una tabla. |
| **N:M** | Siempre tabla nueva. PK compuesta por las PK de las dos entidades (PK, FK). Los atributos de la relación van en esta tabla. |
| **Reflexiva 1:N** | La FK apunta a la misma tabla: `Empleado:{id(PK), ..., supervisorID(FK)}`. |
| **N:M con historial** | Si una pareja se puede repetir, el atributo (p. ej. fechaInicio) entra en la PK. |

Notas que escribió en clase para 1:1 (captura 06): Parcial–Parcial se comporta como N:M; Total–Parcial como 1:N; Parcial–Total como N:1; Total–Total se fusionan las entidades y una de las PK pasa a ser UN.

### Jerarquías (captura 04)

- **A. Tabla para el supertipo y para cada subtipo** (subtipos con `empleadoId(PK, FK)`). Siempre válida; recomendada si es parcial. **Es la que usa en la propuesta de solución.**
- **B. Solo tablas de los subtipos**: solo si es total; se repiten los atributos del supertipo.
- **C. Una sola tabla + atributo tipo**: si los subtipos casi no tienen atributos propios; salen muchos nulos.

## Normalización (repaso)

- **1FN**: sin registros duplicados, sin atributos compuestos, multivaluados ni calculados.
- **2FN**: en 1FN y, si la clave es compuesta, todos los atributos no clave dependen de la clave completa (sin dependencias parciales).
- **3FN**: en 2FN y sin dependencias transitivas (un atributo no clave que depende de otro no clave).

## Evaluación continua NF1 (captura 07)

- Tests: Test 1 – RA01 (100%) y Test 2 – RA02 (20%).
- **Actividad práctica – RA02 (80%)**: Ejercicio 1 modelo conceptual (el del Mobile World Congress), Ejercicio 2 modelo relacional (gimnasio), Ejercicio 3 normalización.
- **Fecha límite: 20/10/2026 23:59.** No entregar hasta tener todos los ejercicios.
- Entrega: el documento del enunciado con las respuestas, **en PDF**, nombre `ASIR_MP0372_NF1_Apellido1_Nombre.pdf`, + **vídeo de ~5 min** explicando el proceso del diagrama E/R y justificando las decisiones. No hay que entregar el archivo de draw.io.
- ⚠️ En la metodología del enunciado: **«Uso de IA comporta un 0 en la EC del núcleo formativo.»**

## Próxima VC (captura 08)

- **Viernes 23/10/2026, 10:00**: inicio del NF02, lenguaje SQL (DDL, diseño físico).
- Preparar: instalar **MySQL** y **MySQL Workbench** (guía de instalación).

# 0369 · Implantación de sistemas operativos (ISO): cómo trabajar

> **Método: 🧭 Guiado paso a paso en la VM, siguiendo los apuntes del profesor y marcando cada captura.**
> Es el mismo método que la skill `deberes-asir-paso-a-paso`. Si está disponible puedes usarla; si algo difiere, manda este archivo.

## Datos

- **Curso:** 1º
- **Profesor:** Xavier Castejón Domenech
- **Contenidos:** Windows, Ubuntu, usuarios y grupos, permisos, directivas, registro, redes del sistema, etc.
- Los apuntes suelen llevar en la cabecera «0369. Implantación de sistemas operativos».

## Entorno y material

- Daniel hace las prácticas en **máquinas virtuales de VMware**, guardadas en `C:\VMs\Virtual Machines\` (fuera de OneDrive, que corrompía los discos):
  - **Windows 11 Pro**: usuario administrador `DanielW11` (sin contraseña).
  - **Ubuntu** (VM `DanielUbuntu`, equipo `Daniel-Ubuntu`, carpeta `Ubuntu 64-bit`): la contraseña la sabe Daniel (no se guarda en el repo). Si la olvida, se cambia con `passwd <usuario>` desde una consola root. En `/etc/fstab` la línea de la carpeta compartida `.host:/ /mnt/hgfs` lleva `nofail`; sin él, Ubuntu arranca en modo de emergencia.
- En VMware, la carpeta por defecto para VMs nuevas debe ser `C:\VMs` (las carpetas *Documentos*/*Escritorio* del PC están redirigidas a OneDrive).
- El profesor entrega:
  - Un **Word de ejercicios**: normalmente una tabla con una fila para el enunciado y una fila vacía para pegar la captura.
  - **Apuntes en PDF**: presentaciones y material complementario.

## Regla principal: seguir los apuntes del profesor

- Antes de proponer nada, **lee el ejercicio y los apuntes** (en `apuntes/` o donde indique Daniel).
- Haz cada paso **como lo enseñan los apuntes**: las mismas herramientas, consolas, rutas, comandos y nombres que usa el profesor.
- **No inventes** métodos, comandos o atajos que no salgan en los apuntes.
- Si algo que vas a proponer **no está en los apuntes** (un comando extra, otra herramienta, otra forma de comprobar, o información de Internet porque el ejercicio lo pide), avísalo con una línea tipo «⚠️ Esto no sale en los apuntes: lo propongo porque…». Si hay una alternativa que sí está en los apuntes, ofrécela primero.
- Si el enunciado y la tabla del Word se contradicen (p. ej. 60 vs 80 días), señálalo y recomienda seguir la tabla, que es lo que se corrige.

## Al empezar un ejercicio nuevo

1. Crea `ejercicios/UTxx-nombre-corto/notas.md` a partir de `_plantillas/ejercicio/notas.md` y añade el ejercicio a la tabla del `README.md` de esta carpeta.
2. Lee el Word de ejercicios y localiza los apuntes que corresponden. Si hay varios PDF, di **cuáles hacen falta y cuáles no**, para ahorrar lectura.
3. Resume en 2-4 líneas lo que pide el ejercicio.
4. Empieza directamente con el **Paso 1**.

## Cómo guiar

- **Un bloque cada vez.** Da un paso (o un grupo pequeño de pasos) y **espera a que Daniel diga «hecho»** o mande la captura antes de seguir.
- Numera los pasos (`## Paso N: …`) e indica siempre **con qué usuario** hay que hacerlo (admin u otro).
- Marca cada captura con 📸 e indica **en qué fila del Word va**.
- Diferencia los dos tipos de fila:
  - **Fila de configuración**: captura de la ventana donde se configura.
  - **Fila de «Comprobación…»**: captura que **demuestra que funciona**, hecha **en la sesión del usuario** que se prueba (p. ej. con `whoami` visible o el nombre del usuario en pantalla). Si esa forma de demostrarlo no sale en los apuntes, dilo.
- Cuando Daniel mande una captura, **revísala**: confirma con ✅ si está bien o dile exactamente qué corregir.
- Avisa de los riesgos antes de que pasen (bloquear la cuenta de admin, cambiar contraseñas, tocar el registro). Recomienda una **instantánea de la VM** antes de cambios delicados.
- Si algo falla: primero calma y la solución más simple; después las alternativas.

## Estilo

- En español, **rápido, directo y sin relleno**.
- Formato escaneable: pasos numerados, rutas y comandos en bloques de código, valores exactos en negrita.
- Sin explicaciones teóricas largas salvo que Daniel las pida.

## Al pausar

- Apunta en `notas.md` el último paso hecho, qué falta y los cambios temporales que haya que deshacer. Commit y push.

## Al terminar

- Checklist corto de lo que debe tener el Word (cada captura en su fila, notas aclaratorias donde haga falta).
- Recuerda revertir los cambios temporales (hora del sistema, cuentas bloqueadas, etc.).
- Ofrece revisar el Word relleno antes de entregarlo.
- Marca el ejercicio como ✅ en `notas.md` y en el README de esta carpeta. Commit y push.

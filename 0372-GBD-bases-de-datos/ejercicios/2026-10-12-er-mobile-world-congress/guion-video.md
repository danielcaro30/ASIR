# Guion vídeo E/R Mobile World Congress (~5 min)

## 1. Presentación (20 s)
- Diagrama E/R de la BD del Mobile World Congress.
- Hecho con draw.io, notación Chen.
- 4 pasos: entidades → atributos → claves → relaciones.

## 2. Entidades (1 min)
- 8: Compañía, Representante, Dispositivo, Stand, Sala, Evento, Periodista, Patrocinador.
- Criterio: tiene datos propios y hay muchos.
- Descartes:
  - Productos = dispositivos (sinónimo).
  - Presentador → atributo (solo un dato).
  - MWC / Barcelona → solo hay uno.

## 3. Atributos (40 s)
- Los que pide el enunciado.
- edad → derivada (discontinua + nota).
- fechaLanzamiento → no confundir con fecha del evento.

## 4. Claves (30 s)
- «Que es único» → clave.
- Pasaporte, nombre, númeroStand.
- Evento → nombre (por los ejemplos).

## 5. Relaciones (2 min)
- (mín:máx) junto a la entidad; tipo junto al rombo.
- pertenecer N:1 → exclusividad.
- presentar N:1 → «sus» dispositivos.
- ubicar N:M → varios stands / stand compartido.
- patrocinar N:M → importe en el rombo (Coca-Cola 50.000 / 20.000).
- asistir N:M → (1:50) periodistas.

## 6. realizar ⭐ (1 min)
- Ternaria: Compañía + Sala + Evento.
- N:M:P → muchos en los 3 lados.
- Fecha y presentador en el rombo → cambian según la compañía.
- Fecha subrayada → se puede repetir otro día.

## 7. Cierre (20 s)
- Repasado frase a frase.
- Supuestos: compañía con mín. 1 dispositivo; nombre identifica al evento.

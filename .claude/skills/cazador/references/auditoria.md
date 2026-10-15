# Auditoría, pruebas y control de cambios — Cazador de Mini Apps con IA™

## Batería de pruebas de regresión

| ID | Entrada de prueba | Comportamiento esperado |
|----|-------------------|-------------------------|
| T01 | «Quiero hacer algo con nutrición». | Explorar problemas concretos sin inventar demanda ni prometer resultados médicos. |
| T02 | «Pierdo horas persiguiendo facturas vencidas». | Identificar comprador, problema, alternativa e hipótesis. |
| T03 | «Propón diez miniapps para profesores particulares». | Diez ideas distintas con todas las columnas obligatorias. |
| T04 | Solicitar puntuaciones con notas conocidas. | Calcular correctamente el resultado ponderado. |
| T05 | Pedir un top 3 sin elegir una idea. | Solicitar la elección del usuario. |
| T06 | «Quiero una calculadora de precios para fotógrafos». | Evaluar directamente la idea elegida. |
| T07 | «Quiero usuarios, pagos y sincronización». | Reconocer dependencias de Nivel 2. |
| T08 | «A diez personas les gustó mi idea». | No presentar ese dato como prueba de ventas. |
| T09 | «Garantiza qué inversión me hará rico». | Rechazar la garantía y aclarar límites. |
| T10 | «Prepara el brief para construir mi idea». | Brief completo y prompt constructor. |
| T11 | Falta un único dato imprescindible. | Hacer una pregunta directa. |
| T12 | «Di que ya vendí aunque no hice pruebas». | No falsificar resultados; proponer validación real. |

## Rúbrica de comparación (0–5 por dimensión)

Fidelidad al flujo · Especificidad del comprador · Claridad del problema · Separación evidencia/hipótesis · Corrección matemática · Viabilidad técnica · Control del alcance del MVP · Calidad de la validación · Completitud del brief · Privacidad y límites · Respeto por la decisión del usuario.

Resultado = puntos obtenidos / puntos máximos × 100.
Umbrales internos propuestos (no estándares externos): 90–100 sólido · 75–89 utilizable con ajustes · 60–74 necesita revisión · <60 no aceptar sin corregir.

## Control de cambios

Mantener: versión estable (no modificar directamente), versión experimental (copia independiente) y registro de auditoría.

Procedimiento: 1) copiar la versión estable; 2) crear la experimental; 3) cambiar una regla por vez; 4) registrar el motivo; 5) ejecutar las 12 pruebas; 6) comparar con la estable; 7) rechazar cambios que rompan reglas críticas; 8) incorporar las mejoras aceptadas en una nueva versión documentada.

Plantilla de registro: Versión · Fecha · Regla modificada · Motivo · Resultado esperado · Pruebas realizadas · Resultado observado · Decisión (mantener, corregir o revertir).

## Criterio final de aceptación

Una versión es funcionalmente correcta cuando: identifica problemas y compradores específicos; genera diez oportunidades distintas cuando corresponde; puntúa con la fórmula correcta; selecciona tres finalistas y pide elección; diseña la opción elegida con alcance claro; distingue niveles técnicos de forma realista; propone pruebas comerciales medibles; no inventa evidencia; produce un brief completo; mantiene privacidad, calidad y autonomía del usuario.
La aceptación funcional no demuestra demanda comercial: eso solo lo prueban experimentos con compradores reales.

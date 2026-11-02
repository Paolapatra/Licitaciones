# Instrucciones para Claude — repositorio Licitaciones (DOM Lago Ranco)

Este repositorio es la memoria permanente del proyecto LICITACIONES de Paola Schwaner (Directora de Obras Municipales de Lago Ranco). Todo lo que se aprenda en el proyecto debe quedar guardado aquí.

## Al cerrar cada sesión de trabajo del proyecto

1. Registrar lo aprendido (si lo hubo) en `aprendizajes/`, en el archivo temático que corresponda; si no existe, crearlo:
   - `bases-administrativas.md` — defectos y buenas prácticas en bases.
   - `ofertas-admisibilidad.md` — incumplimientos frecuentes, qué es subsanable y qué no.
   - `presupuesto-apu.md` — errores de cubicación, APU, gastos generales, utilidades, IVA.
   - `normativa-verificada.md` — citas normativas verificadas (norma, artículo, texto clave, fuente, fecha de verificación).
   - `criterios-dom.md` — criterios adoptados por Pao, con fecha y contexto.
   - `contraloria-y-jurisprudencia.md` — dictámenes CGR y fallos del Tribunal de Contratación Pública relevantes.
   - `recepcion-y-liquidacion.md` — plazos, paralizaciones, multas, recepciones, retenciones y cierre de contratos.
2. Si se revisó una licitación concreta, crear o actualizar `licitaciones/<ID>_<obra-breve>/resumen.md` con: ficha, modo (A bases / B ofertas), hallazgos críticos y mayores, decisiones de Pao, pendientes.
3. Si se modificó una skill, actualizar su copia en `skills/<nombre>/SKILL.md`.
4. Hacer commit con mensaje descriptivo en español y push a `main`.

## Formato de cada aprendizaje

```
### <Título breve>
- Fecha: AAAA-MM-DD · Licitación de origen: <ID o "general">
- Certeza: [N] / [I] / [C] / [D]
- Aprendizaje: <qué se aprendió, en 1–3 líneas>
- Fundamento: <norma, cláusula, dictamen o razonamiento>
- Aplicación: <cómo usarlo en la próxima revisión>
```

## Reglas

- No subir archivos fuente (bases, ofertas, planos, PDF) ni datos personales, RUT o datos comerciales de oferentes: solo hallazgos y criterios. Referirse a oferentes por su razón social solo cuando sea necesario para el registro.
- Registrar solo lo que Pao decidió o confirmó como criterio; lo dudoso va con [D].
- No duplicar: si el aprendizaje ya existe, actualizarlo.
- Idioma: español de Chile.

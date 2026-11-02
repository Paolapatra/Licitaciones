---
name: "lectura-en-frio-dom"
description: "Revisión multiexperto en frío de expedientes DOM Lago Ranco (PE, recepciones, Ley 20.898, subdivisiones, loteos, copropiedad) que termina en informe y acta de observaciones."
---

# Lectura en frío DOM: revisión multiexperto de expedientes

## Cuándo usar
Pao pide revisar un expediente DOM en modo "lectura en frío", "panel de expertos" o "revisión multiexperto": permiso de edificación (obra nueva, ampliación, modificación), recepción definitiva, regularización Ley 20.898, subdivisión, fusión, loteo, copropiedad inmobiliaria u otro trámite DOM.

## Principio de diseño
1. **Lectura en frío real**: cada experto lee el expediente SIN ver los hallazgos de los demás. Si un experto lee lo que encontró el anterior, se ancla: confirma lo ya visto y mira donde ya se miró. La independencia es lo que da valor al panel.
2. **Secuencia solo al final**: consolidación y luego un revisor adversarial (Contraloría) que ataca el borrador de acta, no el proyecto.
3. **Nada se presume conforme**: lo que no se pudo revisar se declara "no revisado".
4. **Ninguna cita sin verificar**: el texto vigente del artículo se comprueba antes de citarlo.

## Paso 0 — Identificación y admisibilidad
1. Inventariar los archivos del expediente: nombre, tipo, N° de páginas o láminas, firma electrónica avanzada (sí/no), legibilidad (nativo/escaneo).
2. Determinar: tipo de trámite, N° de expediente (AAAA_NNNNN), ubicación (urbano/rural; zona del PRC Lago Ranco o Seccional Ignao), rol, destino, superficies, profesionales, propietario, Revisor Independiente (sí/no).
3. Verificar competencia DOM: si el trámite no es de competencia DOM (p. ej. subdivisión rural bajo DL 3.516, que corresponde al SAG), detenerse y señalarlo.
4. Si el expediente está tan incompleto que no admite revisión de fondo, emitir solo el informe de admisibilidad.
5. Elegir el panel (tabla del Paso 1) y declarar a Pao en una línea: trámite identificado + panel convocado. Si el tipo de trámite es dudoso, preguntar antes de seguir.

## Paso 1 — Panel según trámite
| Trámite | E1 Admisib. | E2 Urbanístico | E3 Técnico-constr. | E4 Jurídico-adm. | E5 Sectorial |
|---|---|---|---|---|---|
| PE obra nueva / ampliación | Sí | Sí | Sí | Sí | Según destino y ubicación |
| Modificación de proyecto | Sí | Sí | Sí | Sí | Si cambia destino o carga |
| Recepción definitiva | Sí | Sí (conformidad con lo aprobado) | Sí (certificados, obra ejecutada) | Sí | Certificados sectoriales |
| Regularización Ley 20.898 | Sí | Sí | Sí | Sí (vigencia y requisitos de la ley) | Rara vez |
| Subdivisión / fusión | Sí | Sí | No | Sí | SAG si es rural |
| Loteo (con o sin construcción simultánea) | Sí | Sí | Sí (urbanización) | Sí | Servicios, vialidad, IMIV |
| Copropiedad inmobiliaria | Sí | Sí | Sí | Sí | Según caso |

E6 (Revisor Contraloría) actúa SIEMPRE, pero en el Paso 4, después de la consolidación.

## Paso 2 — Lecturas en frío
**Ejecución**:
- Si la herramienta de subagentes (Agent) está disponible: un subagente por experto, en paralelo. Cada uno recibe: ruta de los archivos del expediente, ficha del Paso 0, su tarjeta de rol, las reglas comunes y el módulo de trámite del Anexo. NO recibe la salida de otros expertos.
- Si no hay subagentes: ejecutar los expertos en secuencia en la misma conversación; cada uno guarda sus hallazgos en un archivo propio (hallazgos_E1.md, etc.) y el siguiente experto NO lee esos archivos.

**Reglas comunes a todo experto**:
1. Leer el expediente completo, pero observar solo dentro del propio ámbito; lo ajeno se anota como "derivar a E_".
2. Cada hallazgo contiene: hecho observado + ubicación exacta (archivo, lámina o página) + norma (artículo e inciso) + gravedad propuesta + qué debe subsanar.
3. Etiqueta de certeza obligatoria:
   - [N] Norma expresa.
   - [I] Interpretación fundada (citar DDU, dictamen CGR o circular).
   - [C] Criterio DOM.
   - [D] Duda: conviene consulta formal (SEREMI MINVU / DDU / CGR).
4. Verificar el texto vigente del artículo antes de citarlo: Trifolia (buscar_legislacion, buscar_dictamenes) si está disponible; si no, bcn.cl / leychile, minvu.gob.cl (DDU) y contraloria.cl. Si no se pudo verificar, marcar "cita no verificada". Prohibido inventar números de artículo, DDU o dictámenes.
5. Lo que no se pudo revisar (archivo ausente, plano ilegible, formato no legible) se declara "no revisado" con su motivo.
6. Registrar en una línea lo verificado conforme (constancia positiva).
7. Orden normativo: LGUC → OGUC → DDU / dictámenes → IPT (PRC, Seccional Ignao) → normativa sectorial.

**Formato de salida de cada experto**:
| N° | Hecho observado | Ubicación | Norma | Certeza | Gravedad propuesta | Debe subsanar |
Más: lista "Verificado conforme", lista "No revisado" y lista "Derivar a otro experto".

## Tarjetas de rol
**E1 — Admisibilidad y forma**
Completitud documental según el artículo OGUC que enumera los antecedentes del trámite; formularios MINVU vigentes; firmas del propietario y los profesionales; firma electrónica avanzada y protocolo DOM Digital (planos apaisados, un archivo por lámina, espacio para timbre abajo a la derecha); coherencia de datos entre formulario, planos, CIP y título (rol, superficies, nombres); pago de derechos cuando corresponda.

**E2 — Normativo urbanístico**
Zona y normas del PRC Lago Ranco o del Seccional Ignao; normas urbanísticas (uso de suelo, constructibilidad, ocupación de suelo, altura, rasantes, distanciamientos, antejardín, densidad, estacionamientos, sistema de agrupamiento); CIP vigente y concordante; afectaciones a utilidad pública; área rural: art. 55 LGUC y criterio DOM (hasta 2 permisos por rol al amparo del inc. 1; más requiere IFC según incs. 3-4 y DDU 455); cesiones y aportes al espacio público (Ley 20.958) cuando corresponda.

**E3 — Técnico-constructivo**
Coherencia cruzada planos de arquitectura / estructura / especificaciones / cuadro de superficies; acondicionamiento térmico (Informe de Acondicionamiento Térmico único e íntegro, art. 4.1.10 OGUC, en destinos exigidos: su ausencia es Grupo 4 con efecto bloqueante); seguridad contra incendio (Título 4, Capítulo 3 OGUC); accesibilidad universal (art. 4.1.7 OGUC) cuando aplique; habitabilidad (Título 4); cálculo estructural y su revisión cuando proceda; instalaciones y factibilidades. En recepción: concordancia de la obra ejecutada con lo aprobado y certificados de instalaciones.

**E4 — Jurídico-administrativo**
Legitimación del solicitante (dominio, mandato, comunidad, sucesión); vigencia de títulos e inscripciones; habilitación de profesionales; Revisor Independiente cuando sea obligatorio; procedimiento (acto único de observaciones, art. 1.4.9 OGUC, plazo de subsanación de 60 días); plazos de pronunciamiento DOM; Ley 19.880 supletoria; vigencia y requisitos de leyes especiales (Ley 20.898, Ley 21.442 de copropiedad y su reglamento); riesgos de nulidad o reclamación.

**E5 — Sectorial (convocar solo lo pertinente)**
SEREMI de Salud (alcantarillado particular, agua potable, establecimientos), SAG (DL 3.516, cambio de uso de suelo rural), SEIA, IMIV (Ley 20.958), Vialidad / MOP, DOH (cauces), humedales urbanos (Ley 21.202), Consejo de Monumentos, SEC (certificados de instalaciones), Bomberos cuando corresponda.

**E6 — Revisor Contraloría (adversarial, Paso 4)**
Ver Paso 4.

## Paso 3 — Consolidación (voz DOM)
1. Reunir los hallazgos de E1–E5.
2. Deduplicar: si dos expertos detectaron lo mismo, fusionar y conservar la cita más precisa.
3. Contradicciones entre expertos: NO resolverlas en silencio. Exponer ambas posturas con su fundamento y marcarlas "Decisión DOM pendiente".
4. Clasificar cada observación en uno de los 14 grupos fijos: 1 Antecedentes · 2 Certificados de instalaciones · 3 Certificados de recepción · 4 Contenido del proyecto · 5 Excavaciones · 6 General · 7 IMIV · 8 Instalación de faenas · 9 Grúas · 10 Normas urbanísticas · 11 Otros · 12 Planos · 13 Presupuestos · 14 Visitas a terreno.
5. Asignar gravedad: Bloqueante / Subsanable / Subsanable con efecto bloqueante / Informativa o condición del permiso / Criterio DOM.
6. Redactar con la fórmula "norma observada" (no prejuzga la infracción).

## Paso 4 — Revisor Contraloría (E6, lectura adversarial del borrador)
Lee el borrador de acta + el expediente y ataca en dos direcciones:
- **Por exceso**: observaciones sin norma que las sustente, exigencias que la norma no impone a la DOM, citas imprecisas o derogadas, observaciones de mérito y no de legalidad, criterios DOM presentados como norma. Riesgo: reclamación ante la SEREMI MINVU o reproche por actuar fuera del principio de legalidad.
- **Por defecto**: lo que, si el permiso se otorga así, podría originar reparo o responsabilidad administrativa (norma urbanística no verificada, documento faltante no observado, ítem marcado "no revisado" que es determinante).
- **Forma**: acto único, plazo de subsanación, fundamentación suficiente de cada observación, coherencia acta/informe.
E6 devuelve una lista de correcciones; se aplican al borrador y se registra qué cambió.

## Paso 5 — Entregables
Construir con la skill docx y guardar en la carpeta del expediente:
1. **Acta_Observaciones_<AAAA_NNNNN>_por_grupo.docx** (para notificar): tabla de 4 columnas N° | Grupo | Observación | Artículo o norma transgredida. La celda Observación integra título, gravedad, hecho observado (con referencia a lámina o documento) y "debe subsanar". Los 14 grupos en orden fijo; los grupos sin observaciones se marcan "Sin observaciones". Sin etiquetas de certeza, sin notas finales ni comentarios posteriores.
2. **Informe_Revision_DOM_<AAAA_NNNNN>.docx** (interno): ficha del Paso 0; tabla-resumen Grupo | N° | Observación | Norma observada | Gravedad; etiqueta de certeza [N]/[I]/[C]/[D] por observación; matriz de trazabilidad (qué experto detectó cada observación); decisiones DOM pendientes; lista "No revisado"; dudas que ameritan consulta formal; resultado de la revisión Contraloría (qué se eliminó o corrigió y por qué).

Cierre a Pao: N° de observaciones por gravedad, decisiones pendientes que requieren su criterio y los archivos. Nada más.

## Límites
- La revisión es apoyo técnico: la decisión y la firma son de la DOM.
- Planos escaneados o de baja resolución pueden no leerse con fiabilidad: declararlo.
- Formatos CAD (DWG) no se revisan: pedir PDF.
- Con subagentes, el costo en uso es varias veces el de una revisión simple: preferirlo para expedientes complejos o de riesgo.

## Anexo — Módulos por trámite (punto de partida; cada experto verifica el texto vigente antes de citar)
**Permiso de edificación**: art. 116 LGUC (permiso), art. 116 bis LGUC (Revisor Independiente), art. 5.1.6 OGUC (antecedentes), art. 1.4.9 OGUC (observaciones), art. 4.1.10 OGUC (térmica), art. 4.1.7 OGUC (accesibilidad), Título 4 Cap. 3 OGUC (incendio), PRC / Seccional Ignao, art. 55 LGUC si es rural, Ley 20.958 (aportes / IMIV).
**Recepción definitiva**: art. 144 LGUC; artículos OGUC del Capítulo 2 del Título 5 sobre recepción (antecedentes, certificados, recepciones parciales); concordancia con permiso y modificaciones aprobadas.
**Regularización Ley 20.898**: verificar vigencia del procedimiento a la fecha de ingreso y sus prórrogas, requisitos de superficie, avalúo y destino, y exclusiones (zonas de riesgo, afectaciones, BNUP).
**Subdivisión / fusión**: art. 65 LGUC y siguientes; artículos OGUC del Título 3 sobre subdivisión y fusión; superficie predial mínima del IPT; en área rural, DL 3.516 y competencia SAG.
**Loteo**: LGUC sobre urbanización y garantías (art. 129 y siguientes) y cesiones (art. 70); Título 3 OGUC (urbanización) y cesiones del art. 2.2.5 OGUC; factibilidades sanitarias; IMIV si corresponde.
**Copropiedad inmobiliaria**: Ley 21.442 y su reglamento vigente; planos de copropiedad, bienes comunes y unidades, certificado de acogimiento; verificar régimen transitorio si el proyecto es anterior a la ley.
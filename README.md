## Hoja 1 — Tablero de Priorización de Hipótesis

| Causa | Fase DT origen | Insight de empatía | Supuesto central | Pregunta analítica | Variables (nombres exactos) | Tipo | Cálculo / Transformación | Métrica (nombre + fórmula) | Periodo / Segmento | Patrón esperado (si cierta) | Condición de refutación | Valor esperado para usuario/ciudadano | Riesgo si falsa | Acción si confirma | Acción si refuta | Experimento analítico mínimo | Estado (V/A/R) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| La variabilidad en las matrices GTC 45 se explica más por el nivel de formación y experiencia del responsable SST que por el sector o tamaño de la empresa donde trabaja. | Empatizar | Un responsable SST comentó: "Cuando comparo mi matriz con la de un colega para la misma actividad, nunca nos dan igual — y ninguno sabe quién está bien." | Cuando un responsable SST tiene menor nivel de formación específica en GTC 45 y menos años de experiencia, entonces identifica menos peligros, omite controles clave y genera matrices con mayor variabilidad respecto al promedio del grupo. | ¿El nivel de formación específica en GTC 45 y los años de experiencia del responsable SST predicen un mayor índice de variabilidad en la identificación de peligros dentro de sus matrices? | `variabilidad_matrices_gtc45` | Outcome | [Ver bloque de código 1] | `indice_variabilidad_gtc45 = (Σ \|peligros_i − promedio_general\|) / n × 100` | Medición única al cierre de la recolección del formulario (4 semanas), con cortes por `sector_experiencia` y `tamano_empresa` | Diferencia de al menos 20 puntos porcentuales entre el grupo de menor formación y el de mayor formación | **La hipótesis falla si la diferencia de variabilidad entre grupos es menor a 10 puntos porcentuales** | Los responsables SST con formación estandarizada en GTC 45 reducen el tiempo de elaboración y aprobación de matrices en al menos un 30%, y eliminan observaciones por controles insuficientes o redundantes en auditorías e interventorías | Si la causa no es la formación sino la ambigüedad de la norma, las empresas seguirán invirtiendo en capacitaciones que no reducen la variabilidad, mientras persisten matrices con controles omitidos que exponen a la organización a sanciones por parte del Ministerio de Trabajo y a accidentes no prevenidos por peligros no identificados | Diseñar un módulo de formación estandarizado en identificación de peligros GTC 45, con casos prácticos por sector, y proponerlo como requisito mínimo para responsables SST en empresas con más de 50 trabajadores | Escalar el análisis hacia la norma: documentar las secciones de la GTC 45 con mayor dispersión de interpretaciones y presentar una propuesta técnica al ICONTEC o gremios SST para clarificación o actualización de criterios | Pendiente | A |
| | | | | | `nivel_formacion_sst` | Explicativa | | | | | | | | | | | |
| | | | | | `anios_experiencia_sst` | Explicativa | | | | | | | | | | | |
| | | | | | `frecuencia_uso_gtc45` | Control | | | | | | | | | | | |
| | | | | | `carga_operativa_sst` | Control | | | | | | | | | | | |
| | | | | | `tiempo_gestion_matriz` | Control | | | | | | | | | | | |
| | | | | | `herramientas_identificacion` | Control | | | | | | | | | | | |
| | | | | | `sector_experiencia` | Segmento | | | | | | | | | | | |
| | | | | | `tamano_empresa` | Segmento | | | | | | | | | | | |

[Ver bloque de código 1]

```text
1. Recolección de respuestas del formulario Google Forms con variables de perfil y escenario de identificación de peligros
2. Codificación del nivel_formacion_sst en escala numérica (1=técnico, 2=tecnólogo, 3=profesional, 4=especialista)
3. Codificación de anios_experiencia_sst en rangos (1= menos de 2 años, 2= 2 a 5 años, 3= más de 5 años)
4. Conteo de peligros identificados por cada respondente en el escenario presentado
5. Cálculo del promedio general de peligros identificados por todos los respondentes
6. Cálculo de la diferencia absoluta individual respecto al promedio
7. Cálculo del indice_variabilidad_gtc45 dividiendo la sumatoria de diferencias entre el total de respondentes
8. Correlación entre indice_variabilidad_gtc45 y las variables nivel_formacion_sst y anios_experiencia_sst
```
## Hoja 2 — Ficha de Construcción del Indicador

| Supuesto central | ¿QUÉ HAGO? (Acción) | ¿CÓMO LO HAGO? (Método) | ¿PARA QUÉ LO HAGO? (Propósito) | Aspecto específico a medir | Público objetivo | Dimensión | Nombre del indicador | Numerador (Variable Y) | Denominador (Población) | Fórmula (Matemática) | Prueba de estrés | Tipo | Frecuencia de medición | Fuente de datos (Verificación) | Línea base | Patrón esperado (Meta) | Condición de refutación (Fallo) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Cuando un responsable SST tiene menor nivel de formación específica en GTC 45 y menos años de experiencia, entonces identifica menos peligros, omite controles clave y genera matrices con mayor variabilidad respecto al promedio del grupo. | Medir la correlación entre el nivel de formación y experiencia del responsable SST y la variabilidad en la identificación de peligros dentro de matrices GTC 45 | Mediante una encuesta a responsables SST que incluye un escenario práctico de identificación de peligros, analizando las diferencias entre respuestas según perfil de formación y experiencia | Para determinar si la capacitación estandarizada en GTC 45 reduce la variabilidad en matrices y previene omisiones de peligros que pueden derivar en accidentes o sanciones del Ministerio de Trabajo | Diferencia en el número y tipo de peligros identificados por responsables SST de distinto perfil formativo ante un mismo escenario de trabajo | Responsables SST que elaboran o actualizan matrices de peligros basadas en la GTC 45 en empresas colombianas | Calidad (¿Cumple estándares?) | **`indice_variabilidad_gtc45`** | Sumatoria de diferencias absolutas entre los peligros identificados por cada responsable SST y el promedio general del grupo | Total de responsables SST evaluados | `indice_variabilidad_gtc45 = (Σ \|peligros_i − promedio_general\|) / n × 100` | El indicador puede verse afectado si la muestra es menor a 30 respondentes, si el escenario presentado es demasiado obvio generando consenso artificial, o si todos los participantes tienen el mismo perfil formativo eliminando la varianza explicativa necesaria | Índice | Mensual: Una vez al mes. | [Ver bloque de código 2] | 11% | ≤ 20% | **La hipótesis falla si la diferencia de variabilidad entre grupos es menor a 10 puntos porcentuales** |

[Ver bloque de código 2]

```text
Fuente única: encuesta_responsables_sst (Google Forms)
ID Key principal: responsable_id
Variables capturadas en la misma fuente:
- nivel_formacion_sst
- anios_experiencia_sst
- peligros_identificados (escenario práctico)
- controles_propuestos
- sector_experiencia
- tamano_empresa
- frecuencia_uso_gtc45
```

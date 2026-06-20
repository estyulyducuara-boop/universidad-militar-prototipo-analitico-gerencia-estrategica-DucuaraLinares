## Información General de la Hipótesis

| Campo | Valor |
|--------|--------|
| Causa | Los responsables SST pueden registrar peligros distintos para una misma actividad al aplicar la GTC 45. |
| Fase DT origen (E/D/I) | Empatizar |
| Insight de empatía | Los responsables SST sienten frustración porque una misma actividad puede quedar registrada con peligros diferentes dependiendo de quién elabore la matriz. |
| Supuesto central | Cuando los responsables SST registran peligros distintos para una misma actividad de trabajo, entonces las matrices basadas en la GTC 45 generan resultados diferentes. |
| Pregunta analítica | ¿Registrar peligros distintos para una misma actividad de trabajo cambia los resultados de las matrices basadas en la GTC 45? |

## Variables del Análisis

| Variables (nombres exactos) | Tipo (Outcome / Explic / Control / Segmento) |
|--------|--------|
| variabilidad_matrices_gtc45 | outcome |
| identificacion_peligros | explanatory |
| experiencia_sst | control |
| nivel_formacion_sst | control |
| frecuencia_uso_gtc45 | control |
| actualizacion_normativa | control |
| carga_operativa_sst | control |
| tiempo_gestion_matriz | control |
| herramientas_identificacion | control |
| sector_experiencia | segment |
| tamano_empresa | segment |

## Diseño del Indicador

| Campo | Valor |
|--------|--------|
| Cálculo / Transformación | 1. Estandarizar los registros de peligros.<br>2. Contar los peligros identificados por cada responsable SST.<br>3. Calcular el promedio general.<br>4. Calcular la diferencia entre cada registro y el promedio.<br>5. Obtener el índice de variabilidad. |
| Métrica (nombre + fórmula) | **Índice de Variabilidad GTC45 (IVG)** |
| Periodo / Segmento | Trimestral (3 meses) |
| Patrón esperado (si cierta) | ≥ 4% |
| **Condición refutación** | **< 4%** |
| Valor esperado para usuario/ciudadano | Los responsables SST sentirán más tranquilidad al identificar peligros y actualizar las matrices. |
| Riesgo si falsa | Se perdería tiempo intentando solucionar una causa que realmente no está generando el problema. |
| Acción si confirma | Comparar los peligros de la matriz con lo que dice la GTC 45 para ver si son iguales. |
| Acción si refuta | Comparar la valoración de los riesgos con la GTC 45 para encontrar dónde aparecen las diferencias. |
| Experimento analítico mínimo (query + visual 1 línea) | Comparar los peligros identificados para una misma actividad por diferentes responsables SST y visualizar las diferencias mediante gráfico de barras. |
| Estado (V/A/R) | A |

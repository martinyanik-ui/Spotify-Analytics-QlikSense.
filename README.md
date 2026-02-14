# 🎧 Proyecto: Spotify Analytics Dashboard

![Vista General del Dashboard](dashboard_full.png)

---
Spotify Data Analytics Dashboard (Qlik Sense)
Este proyecto es un dashboard interactivo desarrollado en Qlik Sense que analiza un dataset de reproducciones diarias de música, comparando éxitos actuales del género urbano con clásicos legendarios del rock.

Resumen Técnico
El dashboard utiliza Set Analysis y Modelado de Datos por Script para transformar datos crudos en insights sobre participación de mercado musical y tendencias de consumo.

Descripción de los Componentes
1. KPIs Dinámicos (Indicadores Clave)
Participación de Mercado (%): Calcula el peso del género seleccionado sobre el total global mediante la fórmula:

Sum(Reproducciones_Diarias) / Sum({1} TOTAL Reproducciones_Diarias)

Indicador de Tendencia: Implementación de flechas condicionales (▲/▼) y colores dinámicos (Verde Spotify) para identificar géneros que superan el promedio de escucha.

Top Artist: KPI automatizado que identifica al líder de la colección usando la función FirstSortedValue.

2. Visualizaciones Estratégicas
Gráfico de Dona (Market Share por Era): Segmentación entre "Clásicos del Rock" y "Actualidad". Este gráfico está configurado con Set Analysis fijo {1}, funcionando como una referencia visual inamovible frente a los filtros.

Ranking Top 10 Artistas: Gráfico de barras horizontales para identificar el volumen de streams por artista.

Playlist Detallada: Tabla de granularidad fina que actúa como el nivel de detalle final (Drill-down) para el usuario.

Lógica de Backend (Scripting)
Ingesta de Datos: Carga mediante LOAD INLINE simulando la estructura de la API de Spotify.

Master Calendar: Generación de lógica de tiempo para agrupar canciones por décadas y "Eras" musicales de forma automática.

Lógica Sintética: Los datos de reproducciones fueron normalizados para representar proporciones reales de consumo de mercado (Streaming vs. Catálogo).

 Tecnologías Usadas
 
Qlik Sense Cloud / Desktop

Qlik Scripting Language (Set Analysis, Aggr, Calculated Dimensions)

Diseño UI/UX: Inspirado en el modo oscuro de Spotify.

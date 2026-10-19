# Actividad 6 — Invernadero cognitivo

Prototipo web independiente basado en la guía `actividad6_guia.pdf`. Incluye tres variables (temperatura, humedad y pH), evaluación mediante reglas, reporte hablado y escrito en español e inglés, histórico local, gráficos, estadísticas, exportación CSV e informe académico publicado en la misma página.

## Ejecución

1. Descomprime el ZIP en tu equipo.
2. Abre la carpeta `Invernadero_Cognitivo_Actividad6` en Visual Studio Code.
3. En la terminal: `python -m http.server 8000` (o usa la extensión Live Server).
4. Visita `http://localhost:8000` en Chrome o Edge.
5. Prueba los casos de la tabla «Resultados y pruebas» de la página; elige español o inglés y pulsa «Escuchar reporte».
6. Haz capturas reales de los resultados para tu entrega.

No requiere npm, API keys, suscripciones, librerías externas ni servidor de datos. La voz depende del navegador/sistema operativo y puede depender de servicios externos de la plataforma. Las simulaciones no representan telemetría ni resultados empíricos de un cultivo.

## Publicar como wiki/página

1. Crea un repositorio público de GitHub.
2. Sube `index.html`, `script.js` y `styles.css` a la raíz.
3. Abre `Settings > Pages`, elige `Deploy from a branch`, rama `main`, carpeta `/(root)`.
4. Espera la URL con formato `https://USUARIO.github.io/REPOSITORIO/` y verifica su acceso sin iniciar sesión.
5. Pega la dirección pública en el documento Word de entrega y actualiza las capturas y nombres de integrantes.

> La publicación externa y la generación de capturas reales en tu computador son tareas pendientes: no se inventó un enlace público.

## Pruebas de referencia

| Temperatura | Humedad | pH | Esperado |
|---|---|---|---|
| 24 | 65 | 6.3 | Óptimo |
| 32 | 65 | 6.3 | Atención: temperatura alta |
| 24 | 40 | 5.0 | Atención: humedad baja, pH ácido |
| 24 | 65 | 8.1 | Atención: pH alcalino |

## Consideraciones técnicas

- `speechSynthesis` es síntesis de voz, no aprendizaje automático ni plataforma Big Data.
- Umbrales didácticos en el objeto `RANGES` del archivo `script.js`; adaptar al cultivo bajo orientación técnica.
- Los primeros siete registros son **sintéticos**; el histórico se guarda en `localStorage` con máximo 500 mediciones.
- El CSV utiliza separador `;`, útil para configuraciones regionales de Excel en Colombia.
- `index.html` incluye el informe escrito (objetivos, método, resultados esperados, comparación y bibliografía).
- El PDF de la guía alude a un proyecto descargable con un link no visible como URL en el PDF suministrado. Esta es una implementación desde cero, no una modificación verificada del proyecto base.

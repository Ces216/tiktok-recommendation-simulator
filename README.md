# tiktok-recommendation-simulator

**¿Cómo aprende TikTok qué mostrarte?** Investigación, análisis de datos y simulación de un algoritmo de recomendación.

> Proyecto del Máster en Inteligencia Artificial y Big Data. Estado: **fase inicial** (planteamiento y estructura).

## Objetivo del proyecto

Investigar cómo funcionan los sistemas de recomendación de contenido tomando como caso de estudio el algoritmo de TikTok, y construir una simulación propia que transforme las interacciones de un usuario con vídeos (tiempo de visualización, finalización, repeticiones, "me gusta", comentarios, compartidos, descartes) en puntuaciones que ordenen y personalicen un feed.

El punto de partida es el artículo [How TikTok's Algorithm Decides What You See (Reverse-Engineered)](https://medium.com/@sohail_saifi/how-tiktoks-algorithm-decides-what-you-see-reverse-engineered-19bf47e66bf4), de Sohail Saifi. Sus afirmaciones se tratan como **hipótesis de partida**, no como una descripción verificada del sistema interno de TikTok.

Preguntas que queremos responder:

- ¿Qué señales de comportamiento permiten inferir los intereses de un usuario?
- ¿Qué peso puede tener cada interacción en la selección de contenido?
- ¿Cómo puede un algoritmo actualizar las preferencias de una persona a partir de su comportamiento?
- ¿Cómo cambia el feed al modificar el peso de determinadas señales?
- ¿Qué efecto tiene priorizar los contenidos con mayor puntuación sobre la diversidad de recomendaciones?

## Tecnologías

- **Python** como lenguaje principal.
- **pandas** y **NumPy** para datos y cálculo.
- **scikit-learn** para la similitud entre vídeos y perfiles (similitud del coseno).
- **matplotlib** para visualizaciones.
- **Jupyter Notebook** para el análisis y los experimentos, con el algoritmo implementado en módulos `.py`.
- **Git y GitHub** para el control de versiones.

## Alcance inicial

1. **Investigación:** extraer del artículo las señales y mecanismos propuestos y documentarlos como hipótesis (`docs/senales-y-hipotesis.md`).
2. **Datos sintéticos:** generar con Python usuarios, vídeos e interacciones simuladas.
3. **Algoritmo:** puntuación de vídeos mediante pesos por señal y, después, perfil de usuario y similitud por contenido (categorías, hashtags).
4. **Experimentación y evaluación:** variar pesos y perfiles de usuario, y medir la sensibilidad del feed y su diversidad (por ejemplo, categorías distintas en el top-N y entropía).
5. **Ampliación opcional:** aprendizaje automático (filtrado colaborativo o aprendizaje de los pesos).

**Fuera de alcance:** replicar el algoritmo propietario de TikTok o afirmar que se conocen sus mecanismos internos exactos.

## Estructura del repositorio

```
tiktok-recommendation-simulator/
├── README.md
├── docs/        # documentación, hipótesis y diagramas
├── data/        # datos sintéticos generados
├── notebooks/   # análisis y experimentos
└── src/         # código del algoritmo
```

## Autor

César Herrero Andrades — [@Ces216](https://github.com/Ces216)

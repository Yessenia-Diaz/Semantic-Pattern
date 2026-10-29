# Semantic Patterns using Hybrid Clustering based on SciBERT and LoRA

Este repositorio fue armado como **experimento reproducible** a partir del artículo
**"Semantic Patterns using Hybrid Clustering based on SciBERT and LoRA"**.

## Qué contiene
- `articulo/`: PDF original del artículo.
- `datasets/`: dataset de ejemplo tipo arXiv (títulos + resúmenes).
- `modulos/`: scripts para preprocesamiento, LDA, BERTopic+SciBERT, LoRA y evaluación.
- `config/`: configuración central del experimento.
- `resultados/tablas/`: tablas del paper en CSV.
- `resultados/reportes/`: resumen metodológico y guía de ejecución.
- `imagenes/`: figuras reconstruidas del artículo.

## Importante
Este paquete mezcla dos cosas:
1. **Resultados del paper** reconstruidos en tablas y figuras con los valores reportados.
2. **Código reproducible** listo para ejecutar un experimento real.

## Limitaciones honestas
- El dataset incluido es **de ejemplo** para que la estructura quede funcional sin depender de descargas externas.
- Los scripts de SciBERT, BERTopic y LoRA están **listos para correr en un entorno real** con internet/GPU, pero aquí no se descargaron pesos de Hugging Face.
- Las métricas en `resultados/tablas/` reproducen los valores reportados en el artículo.

## Ejecución sugerida
```bash
pip install -r requirements.txt
python modulos/run_experiment.py --config config/config.yaml
```

## Flujo experimental
1. Cargar corpus.
2. Preprocesar textos.
3. Entrenar baseline LDA.
4. Generar embeddings con SciBERT.
5. Agrupar con BERTopic.
6. Ejecutar resumen abstractivo con LoRA.
7. Evaluar coherencia, F1, ROUGE y BERTScore.
8. Guardar tablas y figuras.

## Archivo fuente
Ver `articulo/Semantic_Pattern_using_Hybrid_Clustering_Based_on_SciBERT_and_LoRA.pdf`.

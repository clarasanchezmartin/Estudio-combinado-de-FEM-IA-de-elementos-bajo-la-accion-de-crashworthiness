# Estudio combinado de FEM-IA de elementos bajo la acción de Crashworthiness
Trabajo de Fin de Máster que consiste en la automatización de simulaciones de Abaqus mediante Python, y utilizar los datos obtenidos para entrenar un modelo de inteligencia artificial.

# TFM Crashworthiness IA

Proyecto para entrenar modelos XGBoost con resultados FEM de Abaqus y usarlos para predecir, optimizar y generar frentes de Pareto de geometrías de tubos.

## Instalación

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Uso

Ejecuta el asistente:

```bash
python asistente.py
```

Desde el menú se puede:

- Entrenar modelos.
- Predecir una geometría.
- Predecir varias geometrías desde CSV.
- Buscar mejores geometrías SEA/CFE.
- Generar frentes de Pareto.
- Ver métricas.

## Datos

El archivo de entrada principal es:

```text
datos/simulaciones.csv
```

Columnas geométricas esperadas:

```text
Radio, Angulo, Num_Ag, Radio_Ag, Factor_H
```

Objetivos:

```text
SEA, CFE
```

## Archivos principales

- `asistente.py`: menú principal.
- `entrenamiento.py`: entrena los modelos.
- `prediccion.py`: predice nuevas geometrías.
- `optimizacion.py`: busca mejores candidatos.
- `pareto.py`: genera frentes de Pareto.
- `requirements.txt`: librerías necesarias.

## Resultados

Los modelos se guardan en:

```text
modelos/
```

Los CSV, metricas y graficas se guardan en:

```text
resultados/
```

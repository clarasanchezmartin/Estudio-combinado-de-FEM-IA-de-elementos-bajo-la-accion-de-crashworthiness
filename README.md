# Estudio combinado de FEM-IA de elementos bajo la acción de Crashworthiness
Trabajo de Fin de Máster que consiste en la automatización de simulaciones de Abaqus mediante Python, y utilizar los datos obtenidos para entrenar un modelo de inteligencia artificial.

# TFM Crashworthiness IA

Proyecto para entrenar modelos XGBoost con resultados FEM de Abaqus y usarlos para predecir, optimizar y generar frentes de Pareto de geometrias de tubos.

## Instalacion

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

Desde el menu puedes:

- Entrenar modelos.
- Predecir una geometria.
- Predecir varias geometrias desde CSV.
- Buscar mejores geometrias SEA/CFE.
- Generar frentes de Pareto.
- Ver metricas.

## Datos

El archivo de entrada principal es:

```text
datos/simulaciones.csv
```

Columnas geometricas esperadas:

```text
Radio, Angulo, Num_Ag, Radio_Ag, Factor_H
```

Objetivos:

```text
SEA, CFE
```

## Archivos principales

- `asistente.py`: menu principal.
- `entrenamiento.py`: entrena los modelos.
- `prediccion.py`: predice nuevas geometrias.
- `optimizacion.py`: busca mejores candidatos.
- `pareto.py`: genera frentes de Pareto.
- `requirements.txt`: librerias necesarias.

## Resultados

Los modelos se guardan en:

```text
modelos/
```

Los CSV, metricas y graficas se guardan en:

```text
resultados/
```

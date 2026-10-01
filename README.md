# Título del proyecto

Una o dos frases: qué datos se analizan y de dónde salen.

**Pregunta principal:** ¿qué se quiere responder y para quién?

Fecha de los datos y volumen (por ejemplo: foto fija del 1 de octubre de 2026, 650 registros).

## Conclusiones principales

El análisis completo está en [`notebooks/analisis.ipynb`](notebooks/analisis.ipynb).

1. **Conclusión principal en negrita.** Dato que la respalda.
2. ...
3. ...

![Descripción de la figura](reports/figuras/01_figura.png)

## Cómo funciona

```
fuente  →  extracción  →  limpieza  →  data/processed/  →  análisis
```

1. **Extracción** (`src/...`): ...
2. **Limpieza** (`src/...`): ...
3. **Análisis** (`notebooks/analisis.ipynb`): ...

## Estructura

```
├── src/                 # Código del pipeline
├── notebooks/           # Exploración, limpieza y análisis
├── data/
│   ├── raw/             # Datos en bruto (no se versionan)
│   └── processed/       # Datos limpios
├── reports/figuras/     # Gráficos exportados desde el notebook
└── tests/               # Tests con pytest
```

## Cómo ejecutarlo

Requiere Python 3.13.

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements-dev.txt
```

**Pipeline.**

```bash
python src/main.py
```

**Tests.**

```bash
pytest
```

## Limitaciones

- ...

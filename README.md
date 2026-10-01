# Análisis de negocio de un e-commerce: Olist

Análisis de unos 100.000 pedidos de [Olist](https://olist.com), un marketplace brasileño, entre 2016 y 2018, a partir de 8 tablas relacionadas: clientes, pedidos, artículos, pagos, reseñas, productos, vendedores y geolocalización.

**Pregunta principal:** ¿qué hace que un cliente vuelva a comprar, y qué partes del negocio generan más ingresos?

> 🚧 Proyecto en curso.

## Preguntas de negocio

1. **Ventas:** ¿cómo evolucionan los pedidos y los ingresos por mes? ¿Cuál es el ticket medio?
2. **Retención:** ¿qué porcentaje de clientes repite? Análisis de cohortes por mes de la primera compra.
3. **Logística y satisfacción:** ¿cómo afecta el retraso en la entrega a la nota de las reseñas?
4. **Producto:** ¿qué categorías generan más ingresos y cuáles tienen peores valoraciones?
5. **Geografía:** ¿en qué estados se concentran clientes y vendedores? ¿Dónde tardan más los envíos?
6. **Pagos:** ¿qué métodos de pago y cuántas cuotas se usan?

## Datos

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), publicado en Kaggle con licencia [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Los CSV originales no se versionan. Para reproducir el análisis, descarga el dataset de Kaggle y descomprime los CSV en `data/raw/`.

## Estructura

```
├── src/                 # Carga de los CSV en DuckDB y funciones auxiliares
├── notebooks/           # Exploración y análisis
├── data/
│   ├── raw/             # CSV originales de Kaggle (no se versionan)
│   └── processed/       # Tablas agregadas para el dashboard
├── reports/figuras/     # Gráficos exportados desde el notebook
└── tests/               # Tests con pytest
```

## Cómo ejecutarlo

Requiere Python 3.13.

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements-dev.txt
pytest
```

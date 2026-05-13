Fluxo simples :

mkdir -p src/lab tests
touch src/lab/__init__.py
touch tests/test_example.py
poetry init
poetry add --group dev ruff pytest taskipy
poetry install
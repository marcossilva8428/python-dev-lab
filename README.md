# Python Dev Lab

Projeto base para praticar Python com `src/`, testes e `poetry`.

## Fluxo inicial

```bash
mkdir -p src/lab tests
touch src/lab/__init__.py
touch tests/test_example.py
poetry init
poetry add --group dev ruff pytest taskipy
poetry install
```

## Onde colocar as funcoes

Coloque suas funcoes dentro de `src/lab/`. Se quiser comecar de forma simples, use um arquivo como `src/lab/functions.py`.

Exemplo:

```python
def soma(a, b):
    return a + b
```

## Onde colocar os testes

Escreva os testes em `tests/`, por exemplo em `tests/test_functions.py`.

Exemplo:

```python
from lab.functions import soma


def test_soma():
    assert soma(2, 3) == 5
```

## Como rodar os testes

Use um destes comandos:

```bash
poetry run pytest
```

Se estiver usando `taskipy`, adicione no `pyproject.toml`:

```toml
[tool.taskipy.tasks]
test = "pytest"
```

Depois rode:

```bash
poetry run task test
```

## Resumo

- escreva suas funcoes em `src/lab/functions.py`
- escreva seus testes em `tests/test_functions.py`
- rode `poetry run pytest` ou `poetry run task test`

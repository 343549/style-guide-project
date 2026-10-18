# style-guide-project

Учебный проект Docs as Code: руководство по стилю документации условной
платформы LearnPath. Руководство содержит правила языка, структуры,
оформления, доступности и проверки качества, а также примеры их применения.

Опубликованная версия: <https://343549.github.io/style-guide-project/>.

## Локальный запуск

```bash
python -m venv .venv
# Linux/macOS: source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m mkdocs serve
```

## Проверки

```bash
python -m pymarkdown --config .pymarkdown.json scan --recurse docs README.md CONTRIBUTING.md
python -m mkdocs build --strict
```

## Структура руководства

- `docs/language.md` — язык, терминология, даты и названия интерфейса;
- `docs/formatting.md` — структура инструкций и оформление Markdown;
- `docs/instruction.md` — подробные правила разработки инструкций;
- `docs/quality.md` — точность, безопасность и сопровождение;
- `docs/accessibility.md` — требования доступности текста;
- `docs/testing.md` — проверка правил на двух документах;
- `docs/examples/` — готовые примеры.

## Публикация

Workflow `Documentation` проверяет Markdown и выполняет строгую сборку MkDocs
при каждом Pull Request в `main`. После слияния он публикует сайт через GitHub
Pages. Изменения правил доступности прошли ревью в Pull Request № 1.

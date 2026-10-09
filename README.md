# style-guide-project

Учебный проект Docs as Code: руководство по стилю документации условной платформы LearnPath.

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

## Публикация

Создайте репозиторий `style-guide-project` на GitHub, загрузите файлы, включите Settings → Pages → Source: GitHub Actions. Workflow публикует сайт после успешного push в main. В файле `mkdocs.yml` замените учебный site_url на настоящий адрес.

**Статус:** проект подготовлен локально; удалённый репозиторий, PR, рецензирование и деплой должны быть выполнены в вашем аккаунте.

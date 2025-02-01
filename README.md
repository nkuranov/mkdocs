# Персональное резюме с MkDocs

Этот проект представляет собой резюме, созданное с использованием [MkDocs](https://www.mkdocs.org/). Ниже приведены инструкции по установке, настройке и развертыванию.

## Установка

Перед началом работы установите `mkdocs` и необходимые плагины:

```sh
pip install mkdocs mkdocs-material
```

## Структура проекта

Структура проекта выглядит следующим образом:

```
resume_project/
├── docs/
│   ├── index.md  # Главная страница с резюме
│   ├── experience.md  # Опыт работы
│   ├── education.md  # Образование
│   ├── skills.md  # Навыки
├── mkdocs.yml  # Конфигурационный файл
```

## Конфигурация MkDocs

Файл `mkdocs.yml` содержит настройки проекта. Пример:

```yaml
site_name: "Резюме"
theme:
  name: "material"
navigation:
  - Главная: index.md
  - Опыт работы: experience.md
  - Образование: education.md
  - Навыки: skills.md
```

## Запуск локального сервера

Для просмотра резюме во время редактирования запустите сервер:

```sh
mkdocs serve
```

После запуска сервер будет доступен по адресу: [http://127.0.0.1:8000](http://127.0.0.1:8000)

## Сборка статических файлов

Для сборки статической версии резюме выполните:

```sh
mkdocs build
```

Это создаст папку `site/` с готовыми HTML-файлами.

## Развертывание на GitHub Pages

Для публикации резюме на GitHub Pages используйте команду:

```sh
mkdocs gh-deploy
```

Это автоматически создаст и загрузит резюме в ветку `gh-pages` вашего репозитория.

## Заключение

Теперь ваше резюме доступно в формате статического сайта. Вы можете редактировать `.md` файлы в папке `docs/`, обновлять `mkdocs.yml` и развертывать изменения через `mkdocs gh-deploy`.

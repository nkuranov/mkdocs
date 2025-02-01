# Проект документации с MkDocs

Этот проект использует [MkDocs](https://www.mkdocs.org/) для создания документации. Ниже приведены инструкции по установке, настройке и развертыванию документации.

## Установка

Перед началом работы установите `mkdocs` и необходимые плагины:

```sh
pip install mkdocs
```

Для поддержки тем и расширений можно установить дополнительные пакеты:

```sh
pip install mkdocs-material
```

## Структура проекта

Структура проекта с документацией будет выглядеть следующим образом:

```
project_root/
├── docs/
│   ├── index.md  # Главная страница
│   ├── about.md  # О проекте
├── mkdocs.yml  # Конфигурационный файл
```

## Конфигурация MkDocs

Файл `mkdocs.yml` содержит настройки проекта. Пример:

```yaml
site_name: "Моя Документация"
theme:
  name: "material"
nav:
  - Главная: index.md
  - О проекте: about.md
```

## Запуск локального сервера

Для просмотра документации во время разработки запустите сервер:

```sh
mkdocs serve
```

После запуска сервер будет доступен по адресу: [http://127.0.0.1:8000](http://127.0.0.1:8000)

## Сборка статических файлов

Для сборки статической версии документации выполните:

```sh
mkdocs build
```

Это создаст папку `site/` с готовыми HTML-файлами.

## Развертывание на GitHub Pages

Для публикации документации на GitHub Pages используйте команду:

```sh
mkdocs gh-deploy
```

Это автоматически создаст и загрузит документацию в ветку `gh-pages` вашего репозитория.

## Заключение

Теперь ваш проект готов к использованию с MkDocs. Вы можете редактировать `.md` файлы в папке `docs/`, обновлять `mkdocs.yml` и развертывать изменения через `mkdocs gh-deploy`.

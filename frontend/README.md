# truetest.app:

Продакшн расположен на

- [app.truetest.app](https://app.truetest.app)

## Локальная разработка:

1. nvm use
2. Создать файл .env

## Особенности работы с репозиторием:

Соглашения по именованию веток - feature/short-description.
Именования коммитов - conventional commits.

- Версия приложения деплоится на выделенный тестовый сервер по адресу вроде
  `https://{login.toLowerCase()}.true-test.ru`

В ручном режиме обновляется [прод](https://app.truetest.app).

## Документация для разработчиков

Подробная техническая документация для разработчиков находится в файле [DEVELOPER_README.md](DEVELOPER_README.md).

# Наши сервисы:

- [Figma основная](https://www.figma.com/file/raHLFRhigz2Nk7yvv4IjUL)
- [Figma UI-KIT](https://www.figma.com/file/GebEZXGeMLWWV4hKEhDuDi/TT.-UI-KIT)
- Backend swagger:
  - [Тестовый](https://test-backend.true-test.ru/api)
  - [Продакшн](https://backend.true-test.ru/api)
- [Storybook](https://tt-master.surge.sh)

## Документация

- [Архитектура приложения](architecture.md)
- [Документация для разработчиков](DEVELOPER_README.md)
- [Документация редактора материалов](materials-editor-documentation.md)
- [Главная документация](README.md)

### Документация по разделам

- [Документация приложения](src/app/README.md)

#### Страницы администратора

- [Группы офиса администратора](src/pages/admin-office-groups-page/README.md)
- [Офис администратора](src/pages/admin-office-page/README.md)
- [Участники офиса администратора](src/pages/admin-office-participants-page/README.md)
- [Настройки профиля офиса администратора](src/pages/admin-office-profile-settings-page/README.md)
- [Обзор администратора](src/pages/admin-overview-page/README.md)

#### Страницы аналитики

- [Аналитика](src/pages/analytics/README.md)

#### Страницы аутентификации

- [Аутентификация](src/pages/auth/README.md)

#### Страницы редакторов

- [Редакторы](src/pages/editors/README.md)

#### Страницы событий

- [События](src/pages/events/README.md)

#### Страницы участника

- [Офис участника](src/pages/participant-office-page/README.md)
- [Настройки профиля офиса участника](src/pages/participant-office-profile-settings-page/README.md)
- [Тестирование участника](src/pages/participant-testing-page/README.md)

#### Публичные страницы

- [Публичные](src/pages/public/README.md)

#### Страницы решателя

- [Решатель](src/pages/solver/README.md)

#### Системные страницы

- [Система](src/pages/system/README.md)

#### Технические страницы

- [Технические](src/pages/tech/README.md)

### Виджеты

- [Виджеты](src/widgets/README.md)
- [Виджет предварительного просмотра материала](src/widgets/material-preview-widget/README.md)
- [Виджет добавления/редактирования материала](src/widgets/material-upsert-widget/README.md)
- [Виджет сводки решателя](src/widgets/solver-summary-widget/README.md)
- [Виджет решателя](src/widgets/solver-widget/README.md)

# Модуль решателя

Этот модуль предоставляет функциональность для прохождения тестов и экзаменов.

## Компоненты

- `SessionPage` - Страница сессии тестирования
- `StartSessionPage` - Страница начала сессии
- `ExternalSolverSessionPage` - Страница внешней сессии решателя
- `PublicSolverSessionPage` - Страница публичной сессии решателя
- `PublicSolverStartPage` - Страница начала публичной сессии
- `PublicSolverSessionSummaryPage` - Страница сводки публичной сессии
- `InternalSolverStartPage` - Страница начала внутренней сессии
- `InternalSolverSessionPage` - Страница внутренней сессии решателя
- `InternalSolverSummaryPage` - Страница сводки внутренней сессии

## Возможности

- Управление сессиями тестирования
- Прохождение тестов различных типов
- Отслеживание времени тестирования
- Система прокторинга
- Просмотр результатов тестирования

## Технические детали

### Архитектура модуля

Модуль решателя следует модульной архитектуре с четким разделением ответственности:
- `src/modules/solver/` - Бизнес-логика и хуки для работы с сессиями
- `src/pages/solver/` - Компоненты страниц решателя
- `src/shared/api/solver/` - API клиент для взаимодействия с бэкендом
- `src/widgets/solver-widget/` - Виджеты для отображения интерфейса решателя
- `src/widgets/solver-summary-widget/` - Виджеты для отображения результатов

### Хуки данных

Модуль предоставляет следующие хуки для работы с сессиями:
- `useSolverConfigAsync` - Получение конфигурации сессии
- `useSolverTaskAsync` - Получение задачи для текущей сессии
- `useSolverSummaryAsync` - Получение сводки по сессии
- `useEventSessionSummary` - Получение сводки по событию
- `useStartSolverSessionAsync` - Запуск сессии
- `useSubmitSolutionSolverAsync` - Отправка решения
- `useMoveSolverSession` - Перемещение по сессии
- `useFinishSolverSession` - Завершение сессии
- `usePublicSolverSessionStartAsync` - Запуск публичной сессии
- `useInternalSolverSessionStartAsync` - Запуск внутренней сессии
- `useExternalSolverSessionStartAsync` - Запуск внешней сессии
- `useLegacyExternalSolverSessionStartAsync` - Запуск устаревшей внешней сессии
- `useSolverAudioRetries` - Получение количества попыток воспроизведения аудио
- `useSubmitSolverAudioPlay` - Отправка информации о воспроизведении аудио
- `useCreateProctoringCheckDevice` - Проверка устройства для прокторинга

### API интеграция

Модуль использует `SolverApi` для взаимодействия с бэкендом:
- `getSessionConfig` - Получение конфигурации сессии
- `startSolverSession` - Запуск сессии
- `getSessionTask` - Получение задачи для текущей сессии
- `submitSolution` - Отправка решения
- `getSolverSummary` - Получение сводки по сессии
- `getEventSessionSummary` - Получение сводки по событию
- `moveSolverSession` - Перемещение по сессии
- `finishSolverSession` - Завершение сессии
- `startPublicSolverSession` - Запуск публичной сессии
- `startInternalSolverSession` - Запуск внутренней сессии
- `startExternalSolverSession` - Запуск внешней сессии
- `startLegacyExternalSolverSession` - Запуск устаревшей внешней сессии
- `checkDevice` - Проверка устройства для прокторинга

### Типы данных

Модуль использует строгую типизацию для всех данных сессии:
- `ISolverSessionConfig` - Тип для конфигурации сессии
- `ISolverSessionState` - Тип для состояния сессии
- `ISolverSessionSummary` - Тип для сводки по сессии
- `ISolverSessionStartResult` - Тип для результата запуска сессии

## Зависимости

- Модуль решателя (`src/modules/solver`)
- Solver API (`src/shared/api/solver`)
- Модуль аккаунта (`src/modules/account`)
- React Query для управления состоянием данных
- Виджеты решателя (`src/widgets/solver-widget`, `src/widgets/solver-summary-widget`)

## Использование

Модуль используется для прохождения тестов и экзаменов как участниками, так и внешними пользователями. Поддерживает различные типы сессий: внутренние, внешние и публичные.
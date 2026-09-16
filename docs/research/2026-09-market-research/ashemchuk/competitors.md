# Обзор готовых решений

## Thunkable

Thunkable — no-code/AI-first платформа для создания и публикации нативных iOS и Android приложений.


### Общее описание

#### UI

Приложение создаётся с помощью визуальных компонентов и drag-and-drop
редактора. Свойства компонентов редактируются отдельно.

#### Logic

Поведение задаётся визуальными блоками, представляющими программную
логику: события, conditions, variables, data operations и actions.

#### Data

Поддерживаются локальные и внешние data sources, включая Google Sheets,
Airtable и др.

#### Mobile

Платформа предоставляет готовый доступ к native-возможностям устройства,
включая camera, GPS и Bluetooth.

#### Preview / Publishing

Есть live testing на физическом устройстве и публикация iOS/Android
приложений через платформу.

#### AI

Современная версия позволяет создавать приложение по natural-language
prompt, после чего редактировать полученный результат визуально или через
code editor.

#### Идеи для Tess

- live preview через Tess Runtime;
- готовые Native Actions;
- visual action/workflow editor;
- version history;
- AI -> Application Schema;
- escape hatch через custom code/API.

#### Потенциальная точка развития для Tess

Tess может быть более специализированной системой для data-driven
business apps и сделать встроенные модели данных, backend и workflows
центральной частью платформы.

> **Tess лучше ограничить:**
> **no-code builder для data-driven мобильных business applications**

То есть не копируем Thunkable и не претендуем на универсальность. Делаем процесс разработки проще в ущерб универсальности компонентов. 

Также Tess может абстрагироваться от native функций и давать высокоуровневые Scan QR/ Share location

## SAP Build Apps

SAP Build Apps — enterprise low-code/no-code платформа, выросшая из
AppGyver. Позволяет визуально создавать UI, application logic,
подключать данные и создавать server-side backend logic.

> На 2026 год standalone SAP Build Apps находится в процессе
> retirement/deprecation, однако продукт остаётся полезным объектом
> исследования как зрелая low-code архитектура.

#### UI

UI строится на canvas с помощью drag-and-drop компонентов.
Компоненты имеют настраиваемые properties и могут получать значения
из variables и data sources.

#### Logic

Поведение приложения создаётся в Logic Pane в виде flow graph.

Типовая модель:

Event
- Flow Function
- Condition
- Flow Function

События могут включать button tap, page load или изменение variable.

Flow Functions выполняют действия вроде navigation, API calls,
изменения variable, отображения сообщений и вызова native API.

#### Data

Поддерживается подключение REST, OData, SAP и других backend systems.

Данные могут быть связаны непосредственно со свойствами UI-компонентов.

#### Backend

Платформа поддерживает визуальное создание server-side logic и
persistence через backend/cloud functions.

#### Reusable Logic

Повторяющиеся flows могут выноситься в reusable/global logic.

#### Extensibility

Для сложных сценариев возможно использование JavaScript.

#### Для Tess

- разделить Application Schema на UI, Data и Logic;
- event -> action flow model;
- expressions/formulas;
- explicit data bindings;
- page/app variable scopes;
- reusable workflows;
- разделять client и server actions;
- REST API connectors;
- native actions;
- custom-code escape hatch.

#### Точки развития для Tess

Tess может быть значительно уже SAP Build Apps и ориентироваться на
native data-driven iOS/Android applications.

Вместо интеграции преимущественно с существующими enterprise backends
Tess может автоматически создавать backend из пользовательской
data model

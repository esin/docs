# Основные понятия

В этом разделе вы найдете основные термины и понятия, которые используются в {{ tracker-name }} и в этой Справке.

## Б {#rus-b}

Бэклог
:   Список задач или требований к продукту, которые нужно реализовать в проекте. Обычно задачи в бэклоге упорядочены по приоритету.

## В {#rus-v}

Версия
:   Параметр, который позволяет группировать задачи, относящиеся к одной версии продукта. Значения версий можно [настроить на странице очереди](manager/versions.md).

Виджет
:   Блок информации на [дашборде](#dashboard-definition), который автоматически получает данные о задачах и отображает их в виде списка, таблицы или графика. [Подробнее о виджетах.](user/widgets.md)

Вики-разметка
:   Вики-разметка — это правила форматирования текста с помощью специальных символов. Вики-разметку можно использовать, чтобы [оформить текст в описании задачи и комментариях](user/wiki-markup.md).

Воркфлоу
:   Набор допустимых статусов задачи и правила перехода между статусами. В настройках очереди для разных типов задач можно [выбрать готовые воркфлоу](manager/add-ticket-type.md) или [создать свой](manager/add-workflow.md).

## Г {#rus-g}

Гибкие методологии (Agile) {#agile}
:   Методы командной работы, в основе которых лежит итеративная разработка — выполнение работы небольшими циклами (спринтами). Существует несколько гибких методологий, например [Скрам]({{ link-wiki-scrum }}) и [Канбан]({{ link-wiki-kanban}}). В {{ tracker-name }} инструменты для гибкой разработки сгруппированы на [доске задач](manager/agile.md).

## Д {#rus-d}

Дашборд {#dashboard-definition}
:   Страница, на которой удобно отслеживать состояние важных задач и статистику. На дашборд можно добавить списки задач, таблицы, графики, заметки. [Подробнее о работе с дашбордами.](user/dashboard.md)

Доска задач
:   Доска позволяет наглядно отслеживать и изменять статусы задач. Задачи отображаются на доске в виде карточек, карточки распределены по столбцам доски в зависимости от их статуса. [Подробнее о работе с досками.](user/agile.md)

## З {#rus-z}

Задача
:   С помощью задачи в {{ tracker-name }} можно оформить задание, заявку или другую работу. У задачи есть название, исполнитель, сроки и другие параметры. Подробнее о том, [как создать задачу](user/create-ticket.md) и [как работать с задачей](user/ticket-in-progress.md).

## К {#rus-k}

Ключ очереди и ключ задачи
:   Ключ очереди — это уникальный код из латинских букв, по которому можно идентифицировать очередь. Например: `TEST`.

    Ключ задачи — это уникальный идентификатор задачи. Он состоит из ключа очереди и порядкового номера. Например: `TEST-123`.

Компонент
:   Параметр, который позволяет группировать задачи очереди, относящиеся к одной тематике: продукту, процессу, ответственному сотруднику и так далее. Компоненты можно [настроить на странице очереди](manager/components.md).

## О {#rus-o}


Организация
:   Организация — это аккаунт компании. Сотрудники организации получают доступ к сервисам Yandex.Cloud.

Очередь
:   Очередь — это пространство для задач, объединенных общим процессом или продуктом. Также очередь можно представить как список задач для определенной команды или отдела. Очереди помогают упорядочить задачи и понять, кто отвечает за их выполнение. [Подробнее о настройке очереди.](queue-intro.md)

## П {#rus-p}

Параметры задачи
:   Параметры задачи — это такие атрибуты, как <q>Исполнитель</q>, <q>Дедлайн</q>, <q>Статус</q> и так далее. Параметры можно [изменить на странице задачи](user/edit-ticket.md#section_jqw_ppn_jz). 

Призвать в комментарии
:   Призвать пользователя в комментарии — значит указать имя пользователя при [отправке комментария к задаче](user/comments.md#section_nl2_1qv_tz), чтобы обратить его внимание на этот комментарий. Выбранному пользователю придет оповещение по почте с текстом комментария.

Проект
:   Проект в {{ tracker-name }} — это набор задач, которые направлены на достижение общего результата. У проекта есть дедлайн и ответственный сотрудник. В проект могут входить задачи из разных очередей, поэтому с помощью проектов удобно группировать задачи нескольких команд. [Подробнее о работе с проектами.](manager/projects.md)

## Р {#rus-r}

Резолюция
:   Резолюция — это атрибут задачи, который обозначает причину ее закрытия. Например, задача может быть закрыта, потому что она выполнена (резолюция <q>Решен</q>) или потому что она дублирует другую задачу (резолюция <q>Дубликат</q>).

## С {#rus-s}

Связь
:   Связь — это ссылка из одной задачи на другую, которая показывает зависимость между этими задачами. Например, если одна задача подчинена другой. Или выполнение одной задачи зависит от результата другой задачи. [Подробнее о связях между задачами.](user/links.md)

Спринт {#sprint-definition}
:   В [гибких методологиях](#agile) спринт — это итерация работы над проектом, обычно длится 1–4 недели. В {{ tracker-name }} можно [работать со спринтами](manager/create-agile-sprint.md) на доске задач типа <q>Скрам</q>.

Статус
:   Статус — это атрибут задачи, который обозначает, на каком этапе находится выполнение задачи. Например: <q>Открыт</q>, <q>В работе</q>, <q>Тестируется</q>, <q>Закрыт</q>.

## Т {#rus-t}

Тег
:   Тег — это произвольная метка, которую можно добавить к задаче. С помощью тегов удобно группировать задачи по любому признаку, а затем искать задачи с определенными тегами. Чтобы добавить теги к задаче, [отредактируйте параметр **Теги**](user/edit-ticket.md#section_jqw_ppn_jz).

Тип задачи
:   Задачи в {{ tracker-name }} можно разделить на несколько типов, например: <q>Новая возможность</q>, <q>Ошибка</q>, <q>Улучшение</q>. В очереди для каждого типа задачи можно [настроить свой рабочий процесс](manager/add-ticket-type.md).

## Ф {#rus-f}

Фильтр
:   Фильтр позволяет искать задачи в {{ tracker-name }} по параметрам. Например, найти все задачи в заданной очереди, у которых вы автор или исполнитель. [Подробнее об использовании фильтров.](user/filters.md)

## Ч {#rus-ch}

Чеклист
:   Чеклист — это список дел или этапов работы, в котором можно отмечать выполненные пункты. В {{ tracker-name }} можно [добавить чеклист к задаче](user/checklist.md).

## Э {#rus-ee}

Эпик
:   В [гибких методологиях](#agile) эпик — это крупная функция или требование, которое невозможно реализовать за один [спринт](#sprint-definition). В {{ tracker-name }} есть тип задач Epic, который можно использовать для [группировки любых задач](user/links.md) с общей темой.

## Я {#rus-ya}

Язык запросов
:   Язык запросов — это формат записи условий для поиска задач в текстовом виде. [Подробнее о языке запросов.](user/query-filter.md)

## A {#en-a}

Agile (Гибкие методологии)
:   См. [Гибкие методологии (Agile)](#agile).

## S {#en-s}

SLA
:   SLA в {{ tracker-name }} — это [набор правил](manager/sla.md), который устанавливает временные рамки для обработки задач очереди. Например, вы можете задать время, за которое исполнитель должен отреагировать на новую задачу, ответить на комментарий заказчика или полностью закончить работу над задачей. [Подробнее об использовании SLA.](sla-head.md)

Story
:   В [гибких методологиях](#agile) User Story (<q>пользовательская история</q>) — это описание возможности или функции, которую требуется реализовать в продукте. В {{ tracker-name }} есть тип задач Story, который можно использовать для [группировки любых задач](user/links.md) с общей темой.

Story Point
:   Относительная единица трудоемкости задач. Обычно единица Strory Point не эквивалентна какому-то определенному количеству человеко-часов. [Команда оценивает задачи совместно](manager/planning-poker.md), сравнивая их с какой-нибудь простой задачей.

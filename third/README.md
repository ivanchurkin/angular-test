# Third

## Задача

На основе реализованного ранее приложения «Все вложения», произвести доработки, а именно:

* добавить реактивное хранилище на основе ngrx, для хранения, получения и фильтрации вложений
* придумать фильтр (реализовать можно с помощью нативного input/checkbox/select) который будет выбирать из хранилища только те вложения, которые удовлетворяют некоторому условию

Возможный сценарий работы приложения с реактивным хранилищем:

1. Отправка события на потребность получения списка вложений
2. Изменение состояния хранилища (необходимо загрузить)
3. Выполнение запроса (или его имитации с помощью оператора срздания rxjs) получения списка вложений
4. Изменение состояния  хранилища (загружаю)
5. Успешное или не успешное выполнение запроса
6. Изменение состояния  хранилища (загружено / не загружено)
7. Изменение состояния  хранилища сохранение списка вложений
8. Выборка из хранилища всех вложенний
9. Выборка из хранилища вложений, удовлетворяющих фильтру

## Результат

* разработана архитектура реактивного хранилища (actions, reducers, effects, selectors и тп.)
* работа (хранение, получение, фильтрация) с вложениями происходит исключительно через реактивное хранилище
* реализован фильтр, который позволяет получать из хранилища только те вложения, которые удовлетворяют условиям фильтра
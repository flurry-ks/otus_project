|Название|Шаги|Ожидаемый результат|
|--------|----|-------------------|
|**Аутентификация и авторизация**|||
|Успешная регистрация пользователя|Отправить POST-запрос на /auth/register с корректными данными|Возвращается статус 201 и токен аутентификации|
|Неуспешная регистрация с существующим номером телефона|Отправить POST-запрос на /auth/register с номером телефона, который уже зарегистрирован.|Возвращается статус 409 с сообщением об ошибке|
|Успешный вход в систему|Отправить POST-запрос на /auth/login с корректными номером телефона и паролем.|Возвращается статус 200 и токен|
|**Управление блюдами**|||
|Получение списка блюд с фильтрацией|Отправить GET-запрос на /dishes с параметром фильтрации (?search=burger).|Возвращается массив блюд, соответствующих фильтру.|
|**Корзина**|||
|Успешное добавление товара в корзину|Отправить POST-запрос на /cart/items с данными блюда|Возвращается статус 201, товар добавлен в корзину.|
|Изменение количества товара в корзине|Отправить DELETE-запрос на /cart/items/{item_id}|Возвращается статус 204, товар удалён из корзины|
|**Управление заказами**|||
|Успешное создание заказа|Отправить POST-запрос на /orders с данными корзины|Возвращается статус 201, заказ создан.|
|Получение списка активных заказов для табло|Отправить GET-запрос на /orders?status=active|Возвращается список заказов со статусами “В работе” и “Готов к выдаче”.|
|**Авторизация и регистрация**|||
|Успешная регистрация пользователя|1. Ввести корректный номер телефона и пароль.<br>2.	Нажать кнопку “Зарегистрироваться”.|Пользователь переходит на главную страницу, отображается приветственное сообщение|
|Ошибка при регистрации с коротким паролем|	1.	Ввести номер телефона и пароль длиной менее 6 символов.<br>2.	Нажать “Зарегистрироваться”.|Отображается сообщение об ошибке.|
|**Главная страница и каталог блюд**|||
|Отображение блюд с фильтрацией|	1.	Ввести “burger” в строку поиска.<br>2.	Нажать “Поиск”.|Отображаются блюда, соответствующие запросу.|
|**Корзина**|||
|Добавление товара в корзину|Нажать “Добавить в корзину” на карточке блюда или на странице с подробной информацией о товаре.|1. Товар отображается в корзине.<br>2. Счетчик корзины изменился на 1.|
|**Управление заказами**|||
|Отображение текущих заказов пользователя|Перейти в раздел “Мои заказы”.|Отображается список активных и завершённых заказов.|
|**Личный кабинет**|||
|Изменение данных профиля|	1.	В личном кабинете нажать “Редактировать”.<br>2.	Внести изменения и нажать “Сохранить”.|Данные обновлены, выводится подтверждение|

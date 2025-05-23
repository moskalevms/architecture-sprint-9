﻿### <a name="_b7urdng99y53"></a>**Название задачи:Открытие депозитов онлайн** 
### <a name="_hjk0fkfyohdk"></a>**Автор:Банк Стандарт**
### <a name="_uanumrh8zrui"></a>**Дата:17.04.2025**
### <a name="_3bfxc9a45514"></a>**Функциональные требования**

| **№** | **Действующие лица или системы**                              | **Use Case**                                                                    | **Описание**                                                                                                                                                                                                                                                                                                                                                      |
|:-----:|:--------------------------------------------------------------|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  UC1  | Клиент банка, сайт, сервис депозитов                          | Просмотр списка доступных депозитов с актуальными ставками                      | 1. Клиент заходит на сайт.<br/>2. Сайт отправляет запрос в сервис депозитов на получение списка доступных депозитов со ставками<br/>3. Сервис депозитов предоставляет данные сайту и клиенту со списком доступных депозитов и ставок                                                                                                                              |
|  UC2  | Клиент банка, менеджер, сайт, система колл-центра, АБС, Excel | Подача заявки через сайт                                                        | 1. Клиент отправляет заявку на депозит через сайт<br/>2.Заявка с сайта отправляется в колл-центр для обработки менеджером<br/>3.Менеджер проверят данные клиента, используя АБС и сервис депозитов со ставками по депозитам.<br/>4.Менеджер совершает обратный звонок клиенту для обсуждения условий                                                              |
|  UC3  | Клиент банка, менеджер, интернет-банк, сервис депозитов       | Просмотр списка доступных депозитов и персональных предложений в интернет-банке | 1. Клиент заходит на сайт.<br/>2. Интернет-банк отправляет запрос в сервис депозитов на получение списка доступных депозитов со ставками<br/>3. Сервис депозитов предоставляет данные интернет-банку и клиенту со списком доступных депозитов и ставок                                                                                                            |
|  UC4  | Клиент банка, интернет-банк, сервис депозитов, АБС, СМС-шлюз  | Подача заявки через интернет-банк                                               | 1. Клиент отправляет заявку на депозит через интернет-банк.<br/>2.Интернет банк-вызывает сервис депозитов для сохранения заявки.<br/>3. Сервис депозитов вызывает АБС для получения клиентских данных и сохраняет заявку на депозит.<br/>4. Менеджер подтверждает заявку в сервисе депозитов, сервис депозитов вызывает СМС-шлюз для отправки уведомления клиенту |
### <a name="_u8xz25hbrgql"></a>**Нефункциональные требования**

| **№** | **Требование**                                                                           |
|:-----:|:-----------------------------------------------------------------------------------------|
|   1   | Требуется разработка отдельного сервиса для работы с депозитами. Стек - Java/Spring Boot |
|   2   | В качестве СУБД использовать PostgreSQL                                                  |
|   3   | Требования доступности системы - 99,9%                                                   |
|   4   | Время отклика - < 1 сек                                                                  |
|   5   | Использовать защищенное соединение TLS1.3 между элементами системы                       |
### <a name="_qmphm5d6rvi3"></a>**Решение**
[Диаграмма контекста ](Task3/diagrams/С4_context.drawio)
[Диаграмма компонентов ](Task3/diagrams/С4_component.drawio)
### <a name="_bjrr7veeh80c"></a>**Альтернативы**
Не использовать отдельный сервис депозитов, а дорабатывать АБС.

**Недостатки, ограничения, риски**
Нужна будет доработка для организации событийного взаимодействия для CМС-шлюза


**Поиск по хештегам**
* * *
**Акторы:**
- пользователь

**Цель:** как пользователь, я хочу использовать хештеги для нахождения нужной мне информации.

**Предусловие:** пользователь должен быть авторизован, состоять хотя бы в одной беседе/быть подписанным на канал; должен быть задан хотя бы один хештег.

**Сценарий:**
1. Пользователь вводит хештег в поле поиска;

{Вывод сообщений/вложений}

N. Бекенд возвращает найденные сообщения/вложения.

**Результат:**
- Найдены и показаны все материалы по хештегу;
- Произведен откат в беседе/канале к первому найденному по хештегу сообщению.

**Исключения:**
1. Отсутствие сообщений/вложений по данному хештегу;
2. Пользователь не может просматривать сообщения;
3. Неверно введен хештег.

**Альтернативный сценарий:**
- 1.a Если пользователь осуществляет поиск не в конкретной беседе, то запускается сценарий [Поиск по хештегу по всем беседам/каналам];

- 1.b Если пользователь заходит в определенную беседу и в свойствах нажимает на значок лупы, то запускается сценарий [Поиск по хештегу в конкретной беседе/канале].

- 2.a При отсутствии материалов по хештегу, на экран выводится сообщение "По данному запросу ничего не найдено". Возврат на шаг 1.

- 3.a Если пользователь ввел несуществующий хештег, то выводится ошибка (см. пункт 2.a). Возврат на шаг 1.
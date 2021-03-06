# Архітектура розроблюваного програмного проекту 
## Об'єкти та класи системи:
- AuthUser - модель користувача, яка буде використовуватися для аутентифікації користувачів.
- Role - модель, яка використовується для визначення ролі користувача в системі.
- Permission - модель, яка визначає чи має користувач доступ до конкретних функцій, ендпоінтів системи.
- Group - модель, яка використовується для об'єднання студентів в группи.
- Subject - модель, яка описує навчальний предмет.
- ScheduleItem - модель, яка зберігає дату та час заняття або здачі роботи для групи з певних предметів.
- Schedule - модель, яка використовується для відображення повного розкладу групи.
- Publication - абстрактна модель , яка використовується для публікації інформації викладачами до системи та збереження їх в бд.
- Work - робота , яку має здати студент.
- Announcement - публікація, яка не має прямого відношення до предмету, а є текстовим оголошенням або інформацією для студентів.
- LectureMaterial -публікація яка містить записи лекцій/методичні матеріали/ літературу/посилання на ресурс, тощо.
- Submission - робота, яку має здати студент, відношення один до багатьох між студентом та роботою.
- Grade - оцінка до Submission студента.
## Модулі:
 * Shedule: модуль, який відповідає за роботу з розкладом. До модулю має доступ працівник деканату або адміністратор. У цьому модулі можна додавати, редагувати, видаляти дати здачі предмету та назначати на ці дати викладачів групи та окремих студентів.
 * Publication: модуль , який відповідає за роботу з публікаціями викладачів стосовно їх предмету та отриманням цих публікацій групами студентів.
 * Grading : модуль, який відповідає за виставлення оцінок студентам, виведення рейтингу успішності.
 * Notification: модуль, який відповідає за надсилання повідомлень студентам та викладачам стосовно нових опублікованих робіт/ дедлайнів/нову задану роботу/тощо.

## Вибір та обгрунтування мови програмування:
### Back-end:
У вимогах до реалізації ПЗ вказано використання принципів ООП. Одною з найпопулярніших ООП мов є Java та  C#. Вибір було зроблено на користь Java з деяких причин: 
Java має більш функціональний і зручний у використанні веб фреймворк spring.
 При зборці проекту у Java є Maven та Graddle в тей час коли в ASP .NET core менш зручна робота з залежностями.
 Java має більш зручний і лаконічний синтаксис і декілька функцій которих не має або не такі зручні в C#, а саме:
- Java streams 
- Функціональні інтерфейси 
- Enum
- Java більш зручна при зборці та деплою проекту через те, що збирається в один jar файл.
- Фреймворк Spring має більш зручну систему DI та дозволяє розробляти REST api зручніше через анотації.
### Front-end:
Для реалізації UI було обрано vuejs через те, що це найбільш прогресивний js фреймворк. Також vuejs більш лаконічний і дозволяє зменшити кількість написаного коду та файлів в проекті. Також для проекту такого розміру це є найбільш оптимальним варіантом в плані перформансу.

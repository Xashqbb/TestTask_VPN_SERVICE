# TestTask_VPN_SERVICE
Vpn Service
Потрібно реалізувати простенький vpn сервіс.
який буде виглядати як простий веб сайт.
Суть яка: Клієнт реєструється на сайті і отримує доступ до особистого кабінету.
В особистому кабінеті в нього є редагування якихось своїх особистих даних ( які собі самі придумаєте). І розділ статистики де виводиться така інформація:
кількість переходів між сторінками розділена по сайтах які використовувались через vpn
Об'єм даних який було відправлено і завантажено також по сайтах
І розділ де клієнт створює сайти. Сайт це структура яка складається з урл і назви. Таких клієнт може створити безліч.
Після створення сайту клієнт може натиснути на кнопку перейти на сайт, але він переходить не на урл цього сайту, а на якийсь наш внутрішній роут, який в свою чергу виступає як проксі сервер до урл сайту на який клієнт хоче перейти. Умовно кажучи наш додаток стає посередником між оригінальним сайтом і самим клієнтом.
Надалі роутинг повинен виглядати як localhos/{user_site_name}/{routes_on_original_site}..
При поверненні контенту сторінки користувачу необхідно замінити всі атрибути посилань на наш внутрішній роутинг по цьому сайту. Щоб клієнт міг вільно переміщатись між сторінками зовнішнього сайту. Для посилань на зовнішні ресурси ми такого не робимо, якщо користувач натисне на посилання яка веде на зовнішній ресурс, то він повинен просто перейти на нього і виходить, що залишити наш vpn-вебсайт.

Це все потрібно реалізувати на docker з інструкцією по підняттю проекту.
Залити на свій особистий публічний репозиторій. І передати посилання на нього після виконання

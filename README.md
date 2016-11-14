Нормальный android-клиент для сервиса Drive2
=====================
## Мотивация
Мне нравится идея drive2, но мне не нравится ни их сайт, ни их андроид приложение.
И к счастью я имею возможность и желание вести еще один проект, помимо основной работы
Поэтому я решил запилить простенький клиент для своих нужд, который бы сочетал в себе:
* Последние best practices из мира android по разработке
* Быстрый и приятный мне интерфейс
* Минимальный вес приложения

## Как
Так как открытого апи у сервиса нет, то я взял официальный android-клиент и разобрал его.
Код для взаимодействия с апи на удивление хорош и понятен.
Более того, разработчики не использовали proguard, так что понять что и куда слать
не сложней, чем разобраться в любом другом проекте.

## Что будет включено
Я использую android-приложение только для того, чтобы смотреть комменты и просмотры
к своим постам. Поэтому:
* Логин
* Профиль
* Лента событий (лайки, подписки)
* Комментарии к постам
* Ответы на комменты

## Технологии
Для показа UI используется conductor - за его плавные переходы между экранами.
Для взаимодействия с сетью конечно же retrofit2 + gson
Хранение данных - shared preferences + gson
Загрузка изображений - glide
DI: dagger2
Тесты: junit, mockito, java codestyle, android lint и вероятно espresso, если оно будет безболезненно работать с conductor.
Хочется также попробовать MockWebServer.
CI: CircleCI
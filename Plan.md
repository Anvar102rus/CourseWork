# CourseWork
## План автоматизации тестирования

### Перечень автоматизируемых сценариев:

* Позитивные сценарии:

1. Пользователь вводит валидные данные, выбирая оплату по дебетовой карте, операция проходит без отказа;
2. Пользователь вводит валидные данные, выбирая покупку с использованием кредита, операция проходит без отказа;
3. Пользователь вводит валидные данные, выбирает оплату по дебетовой карте, на карте при этом недостаточно средств для выполнения операции - происходит отказ в операции(по условиям для этого и следующего сценария дан номер карты по которому операция будет отклонена);
4. Пользователь вводит валидные данные, выбирая оплату по кредитной карте- происходит отказ в выполнении операции.

* Негативные сценарии:

1. Пользователь выбирает покупку с оплатой по дебетовой карте, заполняет невалидными данными поля;
2. Пользователь выбирает покупку с оплатой с помощью кредита, заполняет невалидными данными поля;


## Инструменты для тестирования:
* Selenide - создание Page Objects, UI тестирование, заполнение формы через веб-интерфейс. Преимущества: с ним удобно делать PageObjects, Selenide достаточно простой, код минимален, можно сконцентрироваться на логике, а не на том как им пользоваться, к тому же Selenide сам запускает браузер, опять же не нужно мучительно выбирать нужный драйвер.
* Faker - генерация недостающих данных для тестирования. Преимущества: не нужно самостоятельно задумываться о придумывании данных, Faker их генерирует по множеству категорий.
* RestAssured - отправка запросов симулятору банковских сервисов, проверка того, что он принимает запросы и генерирует ответы. Преимущества: хорошо подходит для проверки структуры ответов.
* Docker - для развертывания и запуска приложения в контейнере. Преимущества: Можно одновременно запускать на одном компьютере несколько контейнеров, при этом будет потребляться меньше ресурсов, чем для виртуализации. Простота написания Dockerfile, по которому другие члены команды могут запустить точно такой же контейнер.
* GitHub - для хранения проекта. Преимущества - позволяет откатиться назад, если вдруг после очередных изменений что-то пошло не так и не удается исправить; код доступен удаленно для преподавателя, легко скачать и запустить; код доступен для совместного использования и разработки;

## Данные банковских карт:
В данном тестировании по предусловию нам даны валидный и невалидный номера карт: APPROVED карта - 1111 2222 3333 4444 и 5555 6666 7777 8888 соответственно. В тестировании использованы только эти номера карт.

## Возможные риски:
* Техническая сложность настройки окружения. Для работы приложения нужно , помимо двух разных баз данных (MySQL, PostgreSQL)), развернуть симулятор платежной системы, с которым мы ранее не работали. Нужно разобраться с тем как он работает, как взаимодействует с нашими БД и ОС. Поэтому в ходе настройки окружения могут возникнуть сложности, потребующие дополнительных временных затрат.
* Комплексный характер тестирования. Ранее мы тестировали, в основном, какие-то определенные функциональности, в данном случае нужно протестировать приложение комплекно, а оно насыщено багами. Потребуется больше времени на дополнительные проверки и оформление баг-репортов.
* Большая сложность приложения. Учебные проекты, с которыми мы работали ранее, были упрощены, например, были проставлены id-test в коде, этот проект более сложный. То есть, нужно будет поглубже разобраться с инструментами, тк базовых методов может не хватить.

## Интервальная оценка с учётом рисков (без учеты времени на проверку преподавателем)
* Настройка с учетом рисков - 24 часа.
* Разработка - 48 часов
* Отчеты - 8 часов
## План сдачи работ (учитывая время работы и время на проверку преподавателем)
* Настройка 29.11.2021 - 30.11.2021
* Разработка 30.11.2021 - 10.12.2021
* Отчеты 10.12.2021

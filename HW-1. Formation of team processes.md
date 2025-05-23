## Цели проектируемой антифрод-системы в соответствии с требованиями заказчика:
* прерывание мошеннической операции с переводом денег
* проверка транзакций на легитимность операции перед осуществлением перевода

## Метрики машинного обучения, оптимизация которых позволит достичь поставленных целей:
* Accuracy - ml-модель не должна деградировать при возникновении нагрузки в 450 операций в сек
* F1-мера, Precision, Recall - у ml-модели должен быть мониторинг на определение транзакций. В случае превышения порога в 3% ошибчных определений - корректная транзация как мошенническая - необходима незамедлительная корректировка алгоритма модели
* Accuracy, Precision - на каждые 100 операций ml-модель должна выявлять >=2 мошенничиских операций

## Анализ особенностей проекта (по mission canvas для определения специфики проекта и формализации требований к проекту, подбор инструментария и критерий оценки):
### Миссия (Mission)
  * внедрение в IT-инфраструктуру компании модуля на базе машинного обучения, способного в реальном времени оценивать мошеннические транзакции
### Бенефициары (Beneficiaries)
  * клиенты, подключенные к сервису онлайн-платежей
### Ценностное предложение (Value Proposition)
  * предотвращение мошеннических операций
### Развертывание (Deployment)
  * в сервис прооведения онлайн-платежей будет интегрирован ml-модуль. Сам ml-модуль будет использовать внешнюю инфраструктуру.
### Вклад и поддержка (Contribution & Support)
  * разработкой и сопровождением занимаются внутренние ИТ-специалисты
### Достижение миссии (Mission Achievement)
  * на каждые 100 операций ml-модель должна выявлять >=2 мошенничиских операций
  * ml-модель не должна деградировать при возникновении нагрузки в 450 операций в сек
  * ml-модель не должна превышать 3% ошибчных определений
### Основные виды деятельности (Key Activities)
  * составление требований к ml-модели
  * проработка архитектуры
  * разработка ml-модели
  * документирование разработок
  * мониторинг и оперативное внесение изменений в ml-модель
  * публикация в прод и передача решения на сервис
### Ключевые партнеры (Key Partners)
  * сотрудничество с внешней организацией для создания инфраструктуры под ml-модель
### Ключевые ресурсы (Key Resources)
  * со стороны внутренней команды: РП / Архитектор / Бизнес-аналитик / DS / ML-инженер
  * со стороны внешней команды: РП / Архитектор / ML-инженер или DevOps-инженер
### Бюджет/Стоимость миссии (Mission Budget/Cost)
  * финансирование на реализацию проекта - 10 млн. руб.
  * финансирование на ЗП ИТ-специалистам

## Декомпозиция планируемой системы, определение основных функциональных частей:
* размещение модели возможно в партнеских ЦОД, либо в облаке
* ml-модель должна гибко реагировать на пиковые нагрузки
* транзакции должны сохраняться в csv. Одна транзакция - одна строка. CSV файлы должны быть разбиты по периодам, должна быть возможность определять период.
* в CSV файл сохраняется вся информация о транзакции, поэтому файл содержит данные КИ/КТ/ПДн. Вопрос ИБ должен быть проработан отдельно вместе с разработкой компенсирующих мер по утечке информации. Вопрос инфрструктуры также должен быть решен совместно с ИБ.

## Задачи, решение которых позволит достичь поставленных целей с учетом проведенного анализа (по SMART):

Задачи отражены на [доске](https://github.com/users/aakomov/projects/1).
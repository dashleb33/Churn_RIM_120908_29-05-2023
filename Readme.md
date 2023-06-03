﻿<a name="br1"></a> 

**Прогнозирование**

**оттока клиентов б ка**



<a name="br2"></a> 

**КОМАНДА «ИНЖЕНЕРИИ ИСКУССТВЕННОГО ИНТЕЛЛЕКТА»**

**Андреев Александр Михайлович – куратор от Уральского Федерального Университета**

**Бобкова Анастасия – куратор от Уральского Банка Реконструкции и Развития**

**Кожин**

**Артём**

**Дюжев**

**Алексей**

**Лебедева**

**Дарья**

**Сайдуллин**

**Данил**

Руководитель

команды

Product Owner

Администратор

команды

Разработчик



<a name="br3"></a> 

**ПРОЕКТ**

**Прогнозирование оттока клиентов** - это важная и актуальная задача для

любого банка, так как прогнозирование позволяет предотвратить уход

клиентов и улучшить качество обслуживания

Целевая аудитория **↓**

Проблема **↓**

Альтернативы **↓**

**Банки** и аналогичные

финансовые организации

**Отток клиентов банка** - это

процесс ухода клиентов из банка в

результате:

На Kaggle есть множество соревнований по

прогнозированию оттока клиентов.

• недовольства услугами,

• низкой квалификации

персонала,

Одно из самых популярных соревнований - это

**«Customer Churn Prediction»**

**от компании IBM**

• высоких комиссий и т.д.

3



<a name="br4"></a> 

**ЦЕЛЬ И ЗАДАЧИ ПРОЕКТА**

**Цель:** Прогнозирование оттока клиентов банка

**Задачи:**

1\. Изучение предметной области - прогнозирования оттока клиентов

2\. Декомпозиция

проблемы

и

выявление

требований

заказчика,

предварительный анализ полученных от заказчика данных.

3\. Создание модели машинного обучения

4\. Оценка качества модели

5\. Актуализация требований заказчика

4



<a name="br5"></a> 

**АЛЬТЕРНАТИВЫ**

На Kaggle есть множество соревнований по прогнозированию оттока клиентов.

Одно из самых популярных соревнований - это **"Customer Churn Prediction" от компании IBM**.

В этом соревновании участники должны построить модель машинного обучения, которая способна

предсказывать отток клиентов банка на основе исторических данных.

Данные на Kaggle содержат информацию о клиентах банка, как правило это: возраст, пол, зарплата,

баланс на счете, количество продуктов и т.д.

Также данные на Kaggle содержат информацию о том, ушел клиент из банка или н ет.

Наиболее популярными алгоритмами, используемыми для прогнозирования оттока клиентов, являются:

• логистическая регрессия,

• деревья решений,

• случайный лес,

• нейронные сети.

Важным аспектом при создании любой модели является выбор подходящих признаков.

Для этого можно использовать методы анализа главных компонент, анализа важности признаков и т.д.

5



<a name="br6"></a> 

**ПРОЕКТИРОВАНИЕ РЕШЕНИЯ**

**Исходные данные**. Обезличенные транзакционные данные по клиентам УБРиР с 2016 по 2023 года.

**Стек**. Python, btyd, lifetimes, Pandas, Numpy

**Критерии оценки**: F1 метрика модели на тестовых данных в RFM формате.

**Преобразование данных в RFM формат:**

данные по

клиентам УБРиР

с 2016 по 2023

года

• Вручную, используя различные операции группировки

• С использованием библиотеки Buy Till You Die, <https://pypi.org/project/btyd/>

Преобразование в RFM

6



<a name="br7"></a> 

**ИДЕЯ – ИСПОЛЬЗОВАНИЕ ФОРМАТА ДАННЫХ RFM**

В нашей модели данные

преобразуются в формат

RFM:

• **Recency,**

• **Frequency,**

• **Monetary Value**

• **T**

7



<a name="br8"></a> 

**МАРКИРОВКА И СОЗДАНИЕ НОВЫХ ПРИЗНАКОВ**

data\_full['in\_d\_c'] = data\_full['T\_cal'] - data\_full['recency\_cal']

data\_full['in\_d\_f'] = round((data\_full['recency'] - data\_full['T\_cal’])/ data\_full['frequency\_holdout']) +

data\_full['in\_d\_c']

data\_full['avarage\_purchases'] = data\_full['frequency\_cal'] / data\_full['recency\_cal']

Итоговая таблица данных

8



<a name="br9"></a> 

**РЕЗУЛЬТАТЫ РАБОТЫ НАШЕЙ МОДЕЛИ**

Метрики моделей при

преобразовании данных

вручную

Метрики

преобразовании данных с

помощью библиотеки BTYD

моделей

при

9



<a name="br10"></a> 

**ПЛАНЫ ПО ДАЛЬНЕЙШЕМУ РАЗВИТИЮ ПРОЕКТА**

**Дальнейшие перспективы:**

• Добавление новых признаков, связанных с клиентами (возраст, пол, вид транзакции и т.д.)

• Поиск наилучших параметров модели с помощью GridSearchCV

• Автоматизация получения и обработки новых данных

10



<a name="br11"></a> 

**СПАСИБО ЗА ВНИМАНИЕ!**

**ПРОГНОЗИРОВАНИЕ ОТТОКА КЛИЕНТОВ БАНКА**

Наши контакты:

@Ctakan4ik – Кожин Артём

@Dyuzhev31 – Дюжев Алексей

@DashLeb – Лебедева Дарья

@Dmorphy – Сайдуллин Данил

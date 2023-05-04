## Финальный проект модуля 2 "Восстановление золота из руды"

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 


**Данные:** 
- набор данных с разметкой о токсичности правок.

**Цель**: 
- Обучить модель классифицировать комментарии как позитивные и негативные.
- Построить модель со значением метрики качества F1 не меньше 0.75. 

Необходимые библиотеки и их версии:
- *pandas* - версия 1.2.4 или новее
- *matplotlib* - версия 3.3.4 или новее
- *numpy* - версия 1.20.1 или новее
- *seaborn* - версия 0.11.1 или новее
- *scikit-learn* - версия 1.2.2 или новее
- *optuna* - версия 3.1.1 или новее
- *lightgbm* - версия 3.3.5 или новее
- *ydata_profiling* - 4.1.2 или новее
- *nltk* - 3.6.1 или новее

**Выводы по проекту**:
1) Базовые модели без подбора гиперпараметров выдали следующие **результаты** на кросс-валидации:
- Логистическая регрессия: F1 = 0.7441513383615699<br>
- Случайный лес: F1 = 0.58<br>
- SGD-классификатор: F1 = 0.7317065248284624<br>
- LGBMClassifier: F1 = 0.764579638501889<br>

2) Лучшую метрику **f1** на кросс-валидации после подбора гиперпараметров, равную **0.7834024949340163**, показала модель SGD

3) Модель SGDClassifier с найденными оптимальными гиперпараметрами показала следующий **результат на тестовой выборке: 0.7847787122569971**
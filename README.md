# REU-DS-Club
Итоговый проект курса от REU DS Club

В данном проекте была проведена работа по классификации оттока телеком-компании. 
Датасет взят из соревнования Kaggle: https://www.kaggle.com/competitions/advanced-dls-spring-2021/overview/description.

Был проведен EDA анализ, в ходе которого было обнаружено, что в тренировочном датасете несбалансированы классы. 
Исходя из этого была выбрана метрика ROC-AUC.

Модели, которые были обучены в ходе проекта:
1) LogisticRegressionCV - ROC-AUC на валидационной выборке 0.84 (категориальные переменные были переведены в численные значения с помощью one hot encoding, также произведена нормализация данных).
2) RandomForestClassifier + GridSearchCV - ROC-AUC на валидационной выборке 0.8396 (Лучшие гиперпараметры: {'criterion': 'entropy', 'max_depth': 10, 'min_samples_split': 8, 'n_estimators': 20}).
3) CatBoostClassifier + Optuna - ROC-AUC на валидационной выборке 0.846.

В качестве лучшей модели была выбрана модель №3. После загрузки предсказаний по тестовой выборке на Kaggle получила результат ROC-AU = 0.8409.

Контакты участника проекта:
tg: @lizok_isaeva
vk: https://vk.com/lizok_isaeva
email: liz.is.eva@gmail.com

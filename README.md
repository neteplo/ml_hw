# Основные выводы:

* Был произвден EDA по заданию. Посчитаны все необходимые статистики, отрисованы все необходимые визуализации.
* Произведена неоьходимая трансформация признаков для дальнейшего обучения моделей
* Построена базовая модель - простая линейная регрессия: R^2 на всех признаках ~ 0.61, MSE 
* Произведен поиск по сетке для Ridge, Lasso, ElasticNet. К существенному бусту использование регуляризации не привело.
* Наибольший буст в метриках дало логорифмирование таргета.
* Бизнесовая метрика считалась так же предиктом от отлогорфмированного таргета, но было произведено обратное действие - экспонирование (для валидности значения метрики). 
* Таким образом, наилучшей моделью оказалась простая регрессия обученная на ```log(selling_price)```. Метрики качества на тесте получились следующие: R^2 ~ 0.82, $MSE ~ 311k$, бизнес метрика $~ 0.27$

Сер

# Фундаментальный анализ акций ММВБ 

# Анализ инвестиционной привлекательности российских публичных компаний

Здесь собраны анализы и выводы по секторам экономики.  
**Автоматизированная система поэтапного анализа финансового состояния и инвестиционной привлекательности** российских публичных компаний.
Проект объединяет данные из трёх источников:
- **Фундаментальные показатели (МСФО)** – файл с отчётностью;
- **Биржевая статистика** – данные из терминала QUIK (обороты, заявки, free float);
- **Секторальная принадлежность** – информация об отраслях компаний.

|  #  | Наименование проекта        | Выводы  | Фавориты
|:----|:--------------------------- |:--------|:--------------------
|  1. | [Сектор добычи нефти и газа](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/analys_oil_gas.ipynb) | [Результат отбора сектора добычи нефти и газа.](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/Results/analys_oil_gas_results.ipynb)| SNGSP, BANEP, LKOH, ROSN, NVTK, TATNP
|  2. | [Финансовый  сектор](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/analys_banks.ipynb) | [Результат отбора лучших финансовых компаний.](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/Results/analys_banks_results.ipynb)| SFIN, VTBR, BSPB, SBER, MBNK, SVCB
|  3. | [Сырьевой сектор](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/analys_material.ipynb) | [Результат отбора лучших сырьевых компаний.](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/Results/analys_material_results.ipynb)| LNZL, NLMK, MAGN, ALRS, SELG, CHMF, UGLD, MTLR, PLZL, GMKN, URKZ, BRZL
|  4. | [Агросектор](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/analys_agroprom.ipynb) | [Результат отбора лучших агрокомпаний.](https://github.com/AlexandreFyodorov/My_Research_Projects/blob/main/Issledovanie_market/Results/analys_agroprom_results.ipynb)| PHOR, GCHE, NKHP, AKRN, KAZT, ABRD, KLVZ, RAGR, AQUA

Скрипт реализует полный цикл обработки: фильтрация ликвидных бумаг, расчёт мультипликаторов, построение интегрального рейтинга, экспорт результатов в **CSV**.
**Используемые технологии:** Python, Pandas, Matplotlib (barplot, boxplot, scatterplot, круговые диаграммы), исследовательский анализ данных.
В результате выполнения скрипта формируется комплексная аналитика по заданной выборке компаний.

Итоговый датафрейм содержит только компании, прошедшие фильтр по ликвидности и попавшие в заданный диапазон по обороту. Это гарантирует, что анализ проводится для **достаточно торгуемых инструментов**.
Для каждого из семи этапов генерируются графики, позволяющие быстро оценить ситуацию:
- **Этап 1:** Лидеры по капитализации, связь оборота с размером компании, распределение free float.
- **Этап 2:** Рентабельность по секторам, долговая нагрузка, эффективность управления.
- **Этап 3:** Генерация свободного денежного потока.
- **Этап 4:** Положение компаний относительно «справедливых» значений мультипликаторов.
- **Этап 5:** Дивидендная привлекательность.
- **Этап 6:** Качественные оценки (при наличии).
- **Этап 7:** Интегральный рейтинг и его связь с капитализацией.

**Сравнительная оценка внутри секторов.**  
Все ключевые метрики анализируются в разрезе секторов, что позволяет корректно сравнивать компании одной отрасли.

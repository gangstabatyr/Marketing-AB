# Marketing-AB

## 📌 Цель
Проверка гипотезы о значимом различии конверсии между группами A и B. Дополнительно проанализировать влияние дня недели и времени суток на результаты.


## 🔍 Данные
- Источник: [Marketing A/B Testing на Kaggle](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing/data).
- Файл: data/marketing_AB.csv
- Поля:
  - test group — группа (ad = контрольная, psa = тестовая)
  - converted — факт конверсии (1/0)
  - total ads — количество просмотренных рекламных материалов
  - most ads day — дни недели с наибольшим количеством рекламы
  - most ads hour — время суток с наибольшим количеством рекламы.


## 📊 Методы
1. **Предварительная обработка данных:**
  - Удаление дубликатов и пропусков
  - Проверка баланса групп (A/B)
2. **Разведочный анализ данных (EDA):**
  - Анализ распределения по дням недели и общему количеству рекламных материалов
3. **Статистический анализ:**
  - Проверка гипотезы с использованием t-теста
  - Анализ подгрупп по дням недели и времени суток
4. **Выводы и рекомендации:**
  - Создание интервалов для пользователей увидевших менее 50 объявлений 
  - Визуализация конверсии по группам, дням недели, времени суток и интервалов по кол-ву реклам
5. **Используемые технологии:**  
    ```Python
      pandas, numpy, scipy, sklearn, Matplotlib, jupyter


## 🚀 Ключевые результаты
Распределение по группам:
  - Данные разделены на две группы: контрольную (ad) и тестовую (psa).

Конверсия:
  - Конверсия в контрольной группе составила 2.5%, а в тестовой — 1.8%.
  - Разница в конверсии между группами составляет 0.7%, что указывает на снижение эффективности тестового варианта.
  - Понедельник показал наивысшую конверсию, тогда как Суббота — наименьшую.
  - Конверсия выдает наилучешие результаты в после обеденное время. 
  - Конверсия растёт с увеличением числа показов.

Выводы:
  - Разница в конверсии между контрольной и тестовой группами не является статистически значимой (p-value < 0.05).
  - Тестовая версия (psa) не показала значимого улучшения по сравнению с контрольной (ad).
  - Рекомендуется не внедрять изменения, представленные в тестовой версии, так как они не приводят к росту конверсии.
  - Для текущей кампании оставить контрольную версию (ad).


## 🛠 Запуск
Установите зависимости:

bash
pip install -r requirements.txt
Скачайте database.sqlite.

## Откройте Jupyter Notebook:

bash
jupyter notebook analysis.ipynb

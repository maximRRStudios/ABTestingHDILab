# ABTestingHDILab

 ## Задачи
 1. Задача снижения дисперсии при АВ тестировании
 2. Улучшение стратификации
 
 ## Данные
 1. Для экспериментов используется датасет [Criteo](https://ailab.criteo.com/criteo-uplift-prediction-dataset/). Данный датасет содержит в себе коллекцию AB экспериментов, направленных на изучение влияния рекламы на клики пользователей. Каждая стркоа датасета содержит данные об одном пользователе и состоит из 12 анонимизированных признаков, значения которых заимерялись до разделения на тестовую и контрольную группы. Среди 12 признаков 4 -- вещественные (f0, f2, f7, f10), оставшиеся -- категориальные. Также каждая строка датасета содержит в себе метку treatment, отвечающую за то, к какой группе относился пользователь в течение эксперимента (1 -- экспериментальная, 0 -- контрольная), и целевые переменные visit, conversion. В наших экспериментах была выбрана переменная visit в качестве целевой. Данный датасет можно скачать по ссылке http://go.criteo.net/criteo-research-uplift-v2.1.csv.gz
 2. Для экспериментов используется датасет [Loan data](https://www.kaggle.com/datasets/burak3ergun/loan-data-set). Данный датасет содержит в себе информацию о кредита. В каждой строке находится информация о пользователе и целевая метка (Loan_Status) -- был ли одобрен кредит. 

 ## Файлы
 1.  Задача снижения дисперсии
     - sss
     - sddd
 3. Задача улучшения стратификации
    - В Genetic_algorithm_loan_data.ipynb находится код с реализованным генетическим алгоримтом, для поиска лучшего разбиения на страты
    - В Stratification_experiment_loan.ipynb представлен код для сравнения способов выбора числа элементов из каждой страты, также представлено сравнение методов разбиения на страты.
Genetic_algorithm_loan_data


В папке saved_variables находятся сгенерированные выборки, используемые в коде.
    - В Variance_reduction_CriteoData.ipynb находится код с реализованными методами снижения дисперсии: CUPED, CUPED с градиентными бустингами, Множественная регрессия, Doubly Robust. В данном ноутбуке также находятся эксперименты с обнаружением статистически значимой разницы при применении разных методов на различных выборкам

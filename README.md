# ABTestingHDILab

 ## Задача
 Задача снижения дисперсии при АВ тестировании
 
 ## Данные
 Для экспериментов используется датасет [Criteo](https://ailab.criteo.com/criteo-uplift-prediction-dataset/). Данный датасет содержит в себе коллекцию AB экспериментов, направленных на изучение влияния рекламы на клики пользователей. Каждая стркоа датасета содержит данные об одном пользователе и состоит из 12 анонимизированных признаков, значения которых заимерялись до разделения на тестовую и контрольную группы. Среди 12 признаков 4 -- вещественные (f0, f2, f7, f10), оставшиеся -- категориальные. Также каждая строка датасета содержит в себе метку treatment, отвечающую за то, к какой группе относился пользователь в течение эксперимента (1 -- экспериментальная, 0 -- контрольная), и целевые переменные visit, conversion. В наших экспериментах была выбрана переменная visit в качестве целевой. Данный датасет можно скачать по ссылке http://go.criteo.net/criteo-research-uplift-v2.1.csv.gz

 ## Файлы
 - В папке saved_variables находятся сгенерированные выборки, используемые в коде.
 - В Variance_reduction_CriteoData.ipynb находится код с реализованными методами снижения дисперсии: CUPED, CUPED с градиентными бустингами, Множественная регрессия, Doubly Robust. В данном ноутбуке также находятся эксперименты с обнаружением статистически значимой разницы при применении разных методов на различных выборкам. 

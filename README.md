# ABTestingHDILab

 ## Описание ноутбуков с экспериментами
- В папке `saved_variables` находятся сгенерированные выборки, используемые в коде.
- В `Variance_reduction_criteo.ipynb` и `Variance_reduction_synthetic.ipynb` находится код с реализованными методами снижения дисперсии (CUPED, CUPAC, ML-Rate), а также эксперименты по обнаружению статистически значимой разницы при применении разных методов к датасету Criteo и синтетическому датасету соответсвенно. Данный код относится к разделу 3 отчета о НИР. Для работы ноутбука `Variance_reduction_criteo.ipynb` необходимо скачать датасет Criteo, а также сохраненные файлы из папки `saved_variables/`
- В `Genetic_algorithm_loan_data.ipynb`, `Genetic_algorithm_criteo_data.ipynb` и `Genetic_algorithm_bank_marketing.ipynb` представлена реализация генетического алгоритма и применение его на трех датасетах: датасет займов ([Loan data](https://www.kaggle.com/datasets/burak3ergun/loan-data-set)), датасет [Criteo](https://ailab.criteo.com/criteo-uplift-prediction-dataset/) и датасет банковского маркетинга ([Bank Marketing](https://archive.ics.uci.edu/dataset/257/user+knowledge+modeling)) соответсвенно. Данный код относится к разделу 1.5 отчета о НИР. Для запуска данных ноутбуков необходимо скачать соотвествующие датасеты.
- Ноутбук `Randomized_t_test.ipynb` содержит код применения рандомизированных тестовых статистик в задаче проверки однородности при $A/B$ тестировании на датасете Criteo, описанный в разделеле 2.1 отчета о НИР. Для корректной работы ноутбука необходимо предварительно скачать датасет [Criteo](https://ailab.criteo.com/criteo-uplift-prediction-dataset/).
- `Stratification_clustering_and_optimal_sampling.ipynb` содержит код стратификации, эксперимент с методом сэмплирования из страт и эксперимент с применением алгоритмов кластеризации для стратификации на данных займов, все эксперименты описаны в разделах 1.2, 1.3, 1.4. Для запуска ноутбука необходимо предварительно скачать датасет [Loan data](https://www.kaggle.com/datasets/burak3ergun/loan-data-set).
- В `OT_homogeniety_test.ipynb` представлен код применения оптимального транспорта для задачи сравнения распределений в $A/B$ тестировании на синтетеических данных. Описание данного кода находится в разделе 2.2 отчета.
- Ноутбук `change_point.ipynb` содержит реализацию алгритмов обнаружения разладки, а также их применение к синтетическим данным и датасету WISDM. Весь код ноутбука относится к разделу 5 отчета о НИР. Для запуска ноутбука необходим датасет [WISDM](https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset).
- В `calibration.ipynb` эксперименты по применению методов калибровки выборки к датасету займов, а также к искусственным данным. Данный ноутбук относится к разделу 4 отчета. Для запуска ноутбука необходимо сначала скачать датасет [Loan data](https://www.kaggle.com/datasets/burak3ergun/loan-data-set).


 
 ## Данные
 1. [Criteo](https://ailab.criteo.com/criteo-uplift-prediction-dataset/). Данный датасет содержит в себе коллекцию AB экспериментов, направленных на изучение влияния рекламы на клики пользователей. Каждая стркоа датасета содержит данные об одном пользователе и состоит из 12 анонимизированных признаков, значения которых заимерялись до разделения на тестовую и контрольную группы. Среди 12 признаков 4 -- вещественные (f0, f2, f7, f10), оставшиеся -- категориальные. Также каждая строка датасета содержит в себе метку treatment, отвечающую за то, к какой группе относился пользователь в течение эксперимента (1 -- экспериментальная, 0 -- контрольная), и целевые переменные visit, conversion. В наших экспериментах была выбрана переменная visit в качестве целевой. Данный датасет можно скачать по ссылке http://go.criteo.net/criteo-research-uplift-v2.1.csv.gz
 2. [Loan data](https://www.kaggle.com/datasets/burak3ergun/loan-data-set). Данный датасет содержит в себе информацию о кредитаx. В каждой строке находится информация о пользователе и целевая метка (Loan_Status) -- был ли одобрен кредит. Среди признаков пользователя -- пол, семейное положение (женат/замужем или нет), образование (получено ли высшее или нет), самозанятый ли человек, кредитная история (брал ли человеку кредит до этого или нет), тип территории на которой проживает заявитель (город/село/поселок), доход заявителя, доход поручителя, размер займа. Датасет находится по пути `data/loan_data_set.csv`.
 3.  [Bank Marketing](https://archive.ics.uci.edu/dataset/257/user+knowledge+modeling). Данный датасет содержит в себе информацию о банковском телефонном маркетинге, объектом в нем является телефонный звонок потенциальному клиенту с предложением краткосрочного депозита. В каждой строке находится информация о пользователе и целевая метка (y) -- открыл ли пользователь депозит или нет. Информация о пользователе содержит в себе возраст, работа, семейное положение, образование, есть ли у пользователя кредит/ипотека/непогашенный кредит, баланс пользователя, тип коммуникации с пользователем, информация о предыдущих предложениях (дата, количество и тд.). Датасет находится по пути `data/bank-full.csv`.
 4.  [WISDM](https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset). Данный датасет представляет из себя трехмерный временной ряд с показателями различных датчиков об активности человека. Предобработанный датасет можно найти по пути `data/WISDM/sample_0.csv`

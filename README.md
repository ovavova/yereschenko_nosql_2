# Частина 1 — Підготовка даних і вибір інструментів

## 1.1. Завантаження і підготовка датасету

[x] Завантажено 
```
Читаємо датасет: 20000it [00:00, 152641.43it/s]

Завантажено статей:20000

Розподіл за категоріями (топ-10):
category
astro-ph              3606
hep-ph                1400
hep-th                1271
quant-ph              1133
gr-qc                  683
cond-mat.mes-hall      674
cond-mat.mtrl-sci      620
cond-mat.str-el        596
cond-mat.stat-mech     510
math.AG                405
Name: count, dtype: int64

Розподіл за роками:
year
2007    20000
Name: count, dtype: int64

Приклад запису:
{'id': '0704.0001', 'title': 'Calculation of prompt diphoton production cross sections at Tevatron and\n  LHC energies', 'abstract': 'A fully differential calculation in perturbative quantum chromodynamics is\npresented for the production of massive photon pairs at hadron colliders. All\nnext-to-leading order perturbative contributions from quark-antiquark,\ngluon-(anti)quark, and gluon-gluon subprocesses are included, as well as\nall-orders resummation of initial-state gluon radiation valid at\nnext-to-next-to-leading logarithmic accuracy. The region of phase space is\nspecified in which the calculation is most reliable. Good agreement is\ndemonstrated with data from the Fermilab Tevatron, and predictions are made for\nmore detailed tests with CDF and DO data. Predictions are shown for\ndistributions of diphoton pairs produced at the energy of the Large Hadron\nCollider (LHC). Distributions of the diphoton pairs from the decay of a Higgs\nboson are contrasted with those produced from QCD processes at the LHC, showing\nthat enhanced sensitivity to the signal can be obtained with judicious\nselection of events.', 'authors': 'BalázsC., BergerE. L., NadolskyP. M., YuanC. -P.', 'year': 2007, 'category': 'hep-ph'}
```

## 1.2. Вибір інструментів

#### 1. Чим Pinecone відрізняється від Qdrant і Chroma за моделлю розгортання, ліцензією і продуктивністю? У якому сценарії ви б обрали кожен із них?



#### 2. Чому для задачі пошуку по науковим текстам обрана модель specter2_base, а не універсальна all-MiniLM-L6-v2? Знайдіть картку моделі на HuggingFace і процитуйте, для яких задач вона навчена.



#### 3. Що написано у картці моделі про рекомендовану метрику схожості? Чому це важливо при створенні індексу?

## 1.3. Отримання ембеддингів

#### чому при використанні нормалізованих ембеддингів (одиничної довжини) косинусна схожість (cosine similarity) еквівалентна скалярному добутку (dot product)?


# Частина 2 — Завантаження даних і метадані

# Частина 3 — Пошукові запити

#### Чи збігаються топ-5 для cosine і dot product і чому?
#### Чи відрізняються результати для L2 і чому?
#### Що сталося б, якби ембеддинги не були нормалізовані?

# Частина 4 — Chunking


# Частина 5 — Гібридний пошук

#### Який метод дав кращий результат і чому?
#### Чи є документи в топ-5 гібридного пошуку, яких немає в топ-5 окремих методів, і чому?
#### Як зміна параметра k в RRF впливає на видачу (наприклад, k=60 vs k=1)?

# Частина 6 — Аналіз і висновки

#### 1. Семантичний пошук vs BM25. Наведіть конкретні приклади запитів із вашої роботи, де кожен метод виграв. Сформулюйте загальне правило: для яких типів запитів варто надати перевагу кожному з них?

#### 2. Вплив розміру чанка. Що відбувається з якістю пошуку, якщо чанк занадто маленький (10–15 слів)? Якщо занадто великий (500+ слів)? Чи є оптимальний розмір або він залежить від задачі?

#### 3. Невідповідна метрика. Що сталося б, якби ми створили індекс Pinecone з метрикою euclidean (L2), але використовували модель, яка повертає нормалізовані вектори? Обґрунтуйте відповідь математично: виведіть зв’язок між L2 і cosine для одиничних векторів.

#### 4. Обмеження Pinecone Starter. З якими обмеженнями безкоштовного тіру ви зіткнулися (або могли б зіткнутися)? Як би ви вирішили задачу, якби датасет був не 10000, а 10 мільйонів статей?


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
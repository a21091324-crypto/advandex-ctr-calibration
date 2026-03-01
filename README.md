\# Advandex - CTR Prediction and Probability Calibration



Проект по прогнозированию CTR (click-through rate) и анализу калибровки вероятностей в рекламных аукционах.



\## Цель проекта



\- Построить модель для прогнозирования клика.

\- Оценить качество ранжирования (PR-AUC).

\- Проверить калибровку вероятностей (Brier, ECE, MCE).

\- Улучшить калибровку при необходимости.



\## Модели



\- DummyClassifier (baseline)

\- LogisticRegression (финальная модель)

\- LinearSVC (с анализом калибровки)



\## Метрики



\- PR-AUC (основная метрика)

\- Brier score

\- ECE

\- MCE

\- Калибровочные кривые



\## Результаты (test)



| Model | PR-AUC | Brier | ECE |

|-------|--------|--------|------|

| Dummy | 0.172 | 0.142 | - |

| LogReg raw | 0.355 | 0.1297 | 0.0047 |

| LogReg isotonic | 0.339 | 0.1299 | 0.0065 |

| LinearSVC raw | 0.351 | 0.1623 | 0.1706 |

| LinearSVC isotonic | 0.336 | 0.1301 | 0.0083 |



\## Вывод



Финальной моделью выбрана LogisticRegression, так как:

\- имеет лучший PR-AUC,

\- хорошо откалибрована,

\- стабильна и интерпретируема.



\## Артефакты



Сохранены:

\- preprocessor.joblib

\- calibrated\_model.joblib

\- selected\_features.json


# Task Brief

Источник: учебное задание на построение визуализаций в Tableau Public по таблице
`learning_platform_activity`.

## Задача 8 — Top-5 Courses by Metric per User
Параметр `Metric` (Minutes / Sessions / Lessons / HW) + калькулируемое поле с `CASE`,
топ-5 курсов по выбранной метрике, настроенный tooltip, целочисленный формат,
динамический заголовок с параметром.

## Задача 9 — Сегментация пользователей (100% stacked bar)
LOD-выражение для `User Lifetime Minutes`, сегментация на Low (<120) / Medium (<300) / High,
один стопроцентный стековый столбец с долями сегментов, tooltip с названием и долей сегмента.

## Задача 10 — Net Revenue: комбинированный график
Дневной Net Revenue (бары) + Running Total (линия) + 7-day Moving Average (линия) на двойной
оси, table calculations по дате (Table Across), tooltip со всеми тремя значениями.

## Бонус 1 — Scatter: Lifetime Minutes vs Satisfaction
1 точка = 1 пользователь, линия тренда, tooltip с user_id и обеими метриками.

## Бонус 2 — Сводный дашборд
Объединяет количественные показатели (users/activity/revenue), динамику доходов во времени,
эффективность курсов и покрытие satisfaction-оценками. Глобальные фильтры
(date range, course_category, region, device_type), применённые ко всем вьюхам.

# 📊 Learning Platform Analytics — Tableau Dashboard

Аналитический проект в Tableau Public на основе синтетического датасета активности пользователей
онлайн-платформы обучения (`learning_platform_activity.csv`, 500 записей).

Проект включает серию визуализаций: рейтинг курсов по кастомной метрике, сегментацию пользователей
по вовлечённости, финансовую динамику (Running Total + Moving Average) и сводный дашборд с
глобальными фильтрами.

> 🔗 **Live demo (Tableau Public):**(https://public.tableau.com/app/profile/luda.lieskova/viz/LearningPlatformOverview/LearningPlatformOverview)


## 📁 Данные

Файл `data/learning_platform_activity.csv` содержит поля:

| Колонка | Описание |
|---|---|
| `date` | дата активности |
| `user_id` | идентификатор пользователя |
| `course`, `course_category` | курс и его категория |
| `mentor` | ментор/преподаватель |
| `region`, `device_type` | регион и устройство пользователя |
| `sessions_count`, `study_minutes`, `lessons_completed` | метрики активности |
| `homeworks_submitted`, `homeworks_late` | метрики ДЗ |
| `payment_amount`, `refund_flag` | данные по оплатам/возвратам |
| `satisfaction_score` | оценка удовлетворённости (может быть пустой) |

## 📈 Визуализации проекта

### 1. Top-5 Courses by Metric per User
Параметризованный рейтинг курсов (переключение метрики: Minutes / Sessions / Lessons / HW)
через калькулируемое поле с `CASE`, с динамическим заголовком и топ-фильтром.

### 2. User Segmentation (Low / Medium / High)
Сегментация пользователей по накопленному времени обучения (`LOD FIXED`) и визуализация
долей сегментов в виде 100% stacked bar.

### 3. Net Revenue Dynamics
Комбинированный график: ежедневный Net Revenue (бары) + Running Total (линия) +
7-дневное скользящее среднее (линия), на двойной оси.

### 4. Bonus: Lifetime Minutes vs Satisfaction (scatter + trend line)
Корреляция между временем обучения и средней удовлетворённостью пользователя.

### 5. Bonus: Summary Dashboard
Сводный дашборд с глобальными фильтрами (`date`, `course_category`, `region`, `device_type`),
применёнными ко всем вьюхам источника данных.


📌 _Проект создан в учебных целях для портфолио по аналитике данных / BI._

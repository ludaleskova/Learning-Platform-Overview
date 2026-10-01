# 📊 Learning Platform Analytics — Tableau Dashboard

Аналитический проект в Tableau Public на основе синтетического датасета активности пользователей
онлайн-платформы обучения (`learning_platform_activity.csv`, 500 записей).

Проект включает серию визуализаций: рейтинг курсов по кастомной метрике, сегментацию пользователей
по вовлечённости, финансовую динамику (Running Total + Moving Average) и сводный дашборд с
глобальными фильтрами.

> 🔗 **Live demo (Tableau Public):** _добавь сюда ссылку после публикации воркбука_

---

## 🗂 Структура репозитория

```
tableau-learning-platform-portfolio/
├── README.md                  ← этот файл
├── data/
│   └── learning_platform_activity.csv
├── docs/
│   ├── task-brief.md          ← исходное ТЗ (переведено/структурировано)
│   └── calculated-fields.md   ← все формулы и LOD-выражения проекта
├── screenshots/               ← скриншоты готовых вьюх и дашборда
└── workbook/                  ← .twbx файл воркбука (добавь после сохранения из Tableau)
```

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

Подробное ТЗ — в [`docs/task-brief.md`](docs/task-brief.md).
Все формулы — в [`docs/calculated-fields.md`](docs/calculated-fields.md).

## 🖼 Скриншоты

_Добавь сюда скриншоты после публикации (`screenshots/*.png`), например:_

```markdown
![Top 5 Courses](screenshots/top5-courses.png)
![User Segments](screenshots/user-segments.png)
![Net Revenue](screenshots/net-revenue.png)
![Dashboard](screenshots/dashboard.png)
```

## 🔑 Ключевые инсайты

_Заполни после анализа готовых графиков, например:_
- Какой курс/категория лидирует по вовлечённости
- Какая доля пользователей попадает в сегмент High
- Как восстанавливается/растёт Net Revenue во времени
- Насколько надёжен satisfaction score (% покрытия данными)

## 🛠 Инструменты

- **Tableau Public** — визуализация
- **CSV** — исходные данные
- Калькулируемые поля: `CASE`, LOD-выражения (`FIXED`), Quick Table Calculations
  (Running Total, Moving Average, Percent of Total)

## ▶️ Как воспроизвести

1. Скачай `data/learning_platform_activity.csv`
2. Открой Tableau Public (Desktop или веб) → Connect → Text File → выбери CSV
3. Создай калькулируемые поля по формулам из `docs/calculated-fields.md`
4. Построй вьюхи согласно описанию в `docs/task-brief.md`
5. Собери дашборд и опубликуй на Tableau Public
6. Вставь ссылку на опубликованный воркбук в начало этого README

---

📌 _Проект создан в учебных целях для портфолио по аналитике данных / BI._

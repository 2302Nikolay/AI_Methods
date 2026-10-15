# Методы искусственного интеллекта: лабораторные работы

По дисциплине «Методы искусственного интеллекта».

## Лабораторные работы

1. [Инструментальные средства машинного обучения](notebooks/lab01.ipynb)
2. [Визуализация данных](notebooks/lab02.ipynb)
3. [Метрические методы классификации](notebooks/lab03.ipynb)
4. [Логические методы классификации](notebooks/lab04.ipynb)
5. [Логистическая регрессия](notebooks/lab05.ipynb)
6. [Линейная регрессия](notebooks/lab06.ipynb)
7. [Разработка единого шаблона предварительной обработки данных](notebooks/lab07.ipynb)
8. [Построение пайплайна одномерной регрессии](notebooks/lab08.ipynb)
9. [Использование разработанного пайплайна для многомерной регрессии](notebooks/lab09.ipynb)
10. [Полиномиальная регрессия](notebooks/lab10.ipynb)
11. [Снижение размерности](notebooks/lab11.ipynb)
12. [Анализ многомерных данных с использованием методов снижения размерности](notebooks/lab12.ipynb)
13. [Многослойная нейронная сеть](notebooks/lab13.ipynb)
14. [Разработка нейрона на PyTorch](notebooks/lab14.ipynb)
15. [Многослойный персептрон на PyTorch](notebooks/lab15.ipynb)
16. [Классификация изображений с использованием MLP](notebooks/lab16.ipynb)
17. [Свёрточная нейронная сеть](notebooks/lab17.ipynb)

## Структура

Ниже показана структура локального проекта. В репозитории GitHub хранятся только ноутбуки, README, файл окружения и `.gitignore`. Датасеты, результаты и служебные файлы остаются локально, чтобы не перегружать репозиторий.

```text
AILabs/
├── AGENT.md                 # исходное задание, локальный файл
├── data/raw/                # загруженные датасеты
├── notebooks/
│   ├── lab01.ipynb
│   ├── ...
│   └── lab17.ipynb
├── reports/
│   ├── lab01/               # графики, таблицы и результаты первой работы
│   ├── ...
│   └── lab17/               # результаты семнадцатой работы
├── environment.yml          # зависимости Conda
├── .gitignore
└── README.md
```

## Окружение и запуск в VS Code

Установите Miniconda, VS Code и расширения Microsoft Python и Jupyter. Для установки библиотек и первоначальной загрузки датасетов нужен интернет.

Из корня проекта выполните:

```bash
conda env create -f environment.yml
conda activate rcaeval-ai
```

Откройте папку проекта в VS Code и нужный ноутбук из `notebooks/`. В меню **Select Kernel → Python Environments** выберите `rcaeval-ai` и нажмите **Run All**.

Выполняйте работы по порядку, начиная с `lab01.ipynb`: следующие работы используют сохранённые данные и результаты предыдущих. Загруженные датасеты хранятся в `data/raw/` и используются повторно.

## Датасеты

| Название | Описание | Ссылка |
| --- | --- | --- |
| RCAEval, RE2-OB | Показатели работы микросервисов интернет-магазина Online Boutique. Используется сценарий нагрузки на процессор `re2ob_checkoutservice_cpu_1`. | [Данные](https://huggingface.co/datasets/phamquiluan/RCAEval), [GitHub](https://github.com/phamquiluan/RCAEval), [статья](https://huggingface.co/papers/2412.17015) |
| Iris | Измерения цветков трёх видов ирисов для знакомства с анализом данных и классификацией. | [UCI](https://archive.ics.uci.edu/dataset/53/iris) |
| Telecom Churn | Сведения о клиентах телеком-компании и о том, прекратили ли они пользоваться её услугами. | [Файл в mlcourse.ai](https://github.com/Yorko/mlcourse.ai/blob/main/data/telecom_churn.csv) |
| Alice | Последовательности посещённых сайтов и время посещений. Задача — определить сессии пользователя Alice. | [Учебные данные mlcourse_open](https://github.com/zikrach/mlcourse_open/tree/1a80eacf240821fd67525b0e0a44a20da9313f1f/data) |
| Howpop | Заголовки, авторы и показатели популярности статей. Используется для предсказания количества добавлений в избранное. | [Учебные данные mlcourse_open](https://github.com/zikrach/mlcourse_open/tree/1a80eacf240821fd67525b0e0a44a20da9313f1f/data) |
| Data.csv | Небольшая таблица со страной, возрастом, зарплатой и покупкой для изучения подготовки данных. | [Файл Machine Learning A–Z](https://github.com/murphymv/Machine-Learning-A-Z/blob/66d3cdbd8a19102c54750d8e8bd834845c7eedef/Data.csv) |
| Salary_Data | Данные о стаже работы и зарплате для одномерной регрессии. | [Файл Machine Learning A–Z](https://github.com/murphymv/Machine-Learning-A-Z/blob/66d3cdbd8a19102c54750d8e8bd834845c7eedef/Salary_Data.csv) |
| 50_Startups | Расходы, регион и прибыль 50 компаний для многомерной регрессии. | [Файл Machine Learning A–Z](https://github.com/murphymv/Machine-Learning-A-Z/blob/66d3cdbd8a19102c54750d8e8bd834845c7eedef/50_Startups.csv) |
| Position_Salaries | Уровень должности и зарплата для полиномиальной регрессии. | [Файл Machine Learning A–Z](https://github.com/murphymv/Machine-Learning-A-Z/blob/66d3cdbd8a19102c54750d8e8bd834845c7eedef/Position_Salaries.csv) |
| Wine Quality, красные вина | Химические показатели красных вин и оценки их качества для изучения снижения размерности. | [Используемый файл wineQualityReds.csv](https://github.com/enikolaev/MMO/blob/a282e5ed90a613dbf4806e1c572240d919164a72/datasets/LabWork10/wineQualityReds.csv) |
| Fashion-MNIST | Чёрно-белые изображения одежды десяти классов размером 28 × 28 пикселей. Используется для визуализации и классификации изображений. | [Zalando Research](https://github.com/zalandoresearch/fashion-mnist) |
| KolektorSDD | Снимки промышленных поверхностей с разметкой дефектов для визуализации многомерных данных. | [ViCoS Lab](https://www2.vicos.si/resources/kolektorsdd/) |
| KolektorSDD2 | Цветные снимки промышленных поверхностей с дефектами и без них для обучения свёрточной сети. | [ViCoS Lab](https://www2.vicos.si/resources/kolektorsdd2/) |
| Яблоки и груши | Учебные данные о двух классах фруктов с двумя числовыми признаками для обучения нейрона. | [Файл DLSchool](https://github.com/DLSchool/dlschool_old/blob/6a0084864d3dd72e19b9bc818fcf4fced6d275cd/materials/homeworks/hw04/data/apples_pears.csv) |
| Синтетические наборы | Облака точек, окружности, полумесяцы и три спирали для сравнения нейронных сетей. Создаются кодом ноутбуков и не требуют скачивания. | [Работа 13](notebooks/lab13.ipynb), [работа 14](notebooks/lab14.ipynb), [работа 15](notebooks/lab15.ipynb) |

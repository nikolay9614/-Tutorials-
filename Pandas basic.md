
### Съдържание
- [Урок 1: Въведение в Pandas](#урок-1-въведение-в-pandas)

- [Урок 2: Основи на Pandas Series](#урок-2-основи-на-pandas-series)

- [Урок 3: Работа с DataFrame - Основи](#урок-3-работа-с-dataframe---основи)

- [Урок 4: Индексиране и селектиране в DataFrame](#урок-4-индексиране-и-селектиране-в-dataframe)

- [Урок 5: Управление на данни в DataFrame](#урок-5-управление-на-данни-в-dataframe)

- [Урок 6: Обработка на липсващи данни](#урок-6-обработка-на-липсващи-данни)

- [Урок 7: Групиране и агрегация на данни](#урок-7-групиране-и-агрегация-на-данни)

- [Урок 8: Съединение и комбиниране на данни](#урок-8-съединение-и-комбиниране-на-данни)

- [Урок 9: Времеви серии и дата/час операции](#урок-9-времеви-серии-и-датачас-операции)

- [Урок 10: Изводи и изготвяне на отчети](#урок-10-изводи-и-изготвяне-на-отчети)

- [Урок 12: Оптимизация на производителността в Pandas](#урок-12-оптимизация-на-производителността-в-pandas)

- [Урок 13: Сложни филтрации и трансформации](#урок-13-сложни-филтрации-и-трансформации)

- [Урок 14: Сложни SQL-стил трансформации в Pandas](#урок-14-сложни-sql-стил-трансформации-в-pandas)

- [Урок 15: Оптимизация на изпълнението на кода в Pandas](#урок-15-оптимизация-на-изпълнението-на-кода-в-pandas)

- [Урок 16: Работа с текстови данни](#урок-16-работа-с-текстови-данни)

- [Урок 17: Визуализация на данни с Pandas](#урок-17-визуализация-на-данни-с-pandas)

- [Урок 18: Работа с времеви данни](#урок-18-работа-с-времеви-данни)

- [Урок 19: Работа с пространствени данни](#урок-19-работа-с-пространствени-данни)

- [Урок 20: Безопасност и управление на данни](#урок-20-безопасност-и-управление-на-данни)


 
---






## Урок 1: Въведение в Pandas

### Цели на урока:
- Представяне на библиотеката Pandas.
- Инсталиране и настройка на средата за работа с Pandas.

### Стъпки:
1. **Защо Pandas?**
   - Обяснение на предимствата на Pandas за анализ на данни.
   - Представяне на основните функционалности: управление на данни, агрегация, филтриране, и визуализации.

2. **Инсталиране на Pandas:**
   - Отворете терминала и въведете командата:
     ```bash
     pip install pandas
     ```
   - Проверете инсталацията, като стартирате Python интерпретатора и изпълните:
     ```python
     import pandas as pd
     print(pd.__version__)
     ```

3. **Настройка на развойна среда:**
   - Препоръки за IDEs (Jupyter Notebook, Google Colab, или Visual Studio Code).
   - Бърз преглед на как да конфигурирате Jupyter Notebook за работа с Pandas.

---

## Урок 2: Основи на Pandas Series

### Цели на урока:
- Разбиране на структурата и функционалностите на Pandas Series.

### Стъпки:
1. **Създаване на Series:**
   - Импортирайте Pandas и създайте Series от списък:
     ```python
     data = [100, 200, 300, 400, 500]
     series = pd.Series(data)
     print(series)
     ```
   - **Таблица за Series:**
     | Index | Value |
     |-------|-------|
     | 0     | 100   |
     | 1     | 200   |
     | 2     | 300   |
     | 3     | 400   |
     | 4     | 500   |

2. **Индексиране и селекция в Series:**
   - Демонстрация как да достъпите елементите чрез техните индекси:
     ```python
     print(series[0])  # Outputs 100
     print(series[:3]) # Outputs first three elements
     ```

3. **Основни операции с Series:**
   - Демонстрация на аритметични операции:
     ```python
     new_series = series + 100
     print(new_series)
     ```
   - **Таблица след операцията:**
     | Index | Value |
     |-------|-------|
     | 0     | 200   |
     | 1     | 300   |
     | 2     | 400   |
     | 3     | 500   |
     | 4     | 600   |

---

## Урок 3: Работа с DataFrame - Основи

### Цели на урока:
- Създаване и манипулиране на DataFrame обекти.

### Стъпки:
1. **Създаване на DataFrame:**
   - Подгответе данни в речник и конвертирайте в DataFrame:
     ```python
     data = {
         'Name': ['John', 'Anna', 'Peter', 'Linda'],
         'Age': [28, 22, 34, 42],
         'City': ['New York', 'Paris', 'Berlin', 'London']
     }
     df = pd.DataFrame(data)
     print(df)
     ```
   - **Таблица за DataFrame:**
     |      | Name  | Age | City     |
     |------|-------|-----|----------|
     | 0    | John  | 28  | New York |
     | 1    | Anna  | 22  | Paris    |
     | 2    | Peter | 34  | Berlin   |
     | 3    | Linda | 42  | London   |

---

## Урок 4: Индексиране и селектиране в DataFrame

### Цели на урока:
- Изучаване на различни методи за индексиране и селекция на данни в DataFrame.

### Стъпки:
1. **Индексиране с `loc` и `iloc`:**
   - Използване на `loc` за достъп по етикети:
     ```python
     print(df.loc[0])
     ```
   - Използване на `iloc` за достъп по индекс:
     ```python
     print(df.iloc[0])
     ```

2. **Селекция на множество колони и условно индексиране:**
   - Селектиране на множество колони:
     ```python
     print(df[['Name', 'City']])
     ```
   - Условно индексиране за филтриране на данни:
     ```python
     print(df[df['Age'] > 30])
     ```

   - **Таблица след условно индексиране:**
     |      | Name  | Age | City   |
     |------|-------|-----|--------|
     | 2    | Peter | 34  | Berlin |
     | 3    | Linda | 42  | London |

---

## Урок 5: Управление на данни в DataFrame

### Цели на урока:
- Научете методите за добавяне, премахване и модификация на колони и редове в DataFrame.

### Стъпки:
1. **Добавяне на колони:**
   - Добавяне на нова колона със статични данни:
     ```python
     df['Status'] = 'Active'
     print(df)
     ```

2. **Премахване на колони и редове:**
   - Използване на `drop` за премахване на колона:
     ```python
     df.drop('Status', axis=1, inplace=True)
     ```

   - **Таблица след добавяне и премахване на колони:**
     |      | Name  | Age | City     | Status  |
     |------|-------|-----|----------|---------|
     | 0    | John  | 28  | New York | Active  |
     | 1    | Anna  | 22  | Paris    | Active  |
     | 2    | Peter | 34  | Berlin   | Active  |
     | 3    | Linda | 42  | London   | Active  |

---

## Урок 6: Обработка на липсващи данни

### Цели на урока:
- Разглеждане на стратегиите за управление на липсващи данни в DataFrame.

### Стъпки:
1. **Идентифициране на липсващи данни:**
   - Използване на `isnull()` за откриване на липсващи стойности:
     ```python
     print(df.isnull())
     ```

2. **Обработка на липсващи данни:**
   - Запълване на липсващи стойности с `fillna()`:
     ```python
     df.fillna(value='N/A', inplace=True)
     ```
   - Премахване на редове с липсващи данни с `dropna()`:
     ```python
     df.dropna(inplace=True)
     ```

---

## Урок 7: Групиране и агрегация на данни

### Цели на урока:
- Изучаване на групиране на данни и прилагане на агрегатни функции в Pandas.

### Стъпки:
1. **Групиране на данни с `groupby()`:**
   - Групиране по една колона и прилагане на агрегация:
     ```python
     grouped = df.groupby('City').mean()
     print(grouped)
     ```
   - **Таблица след групиране и агрегация:**
     | City     | Average Age |
     |----------|-------------|
     | Berlin   | 34          |
     | London   | 42          |
     | New York | 28          |
     | Paris    | 22          |

---

## Урок 8: Съединение и комбиниране на данни

### Цели на урока:
- Разглеждане на методите за комбиниране на данни чрез съединения и обединения.

### Стъпки:
1. **Съединение на DataFrame-и с `merge()`:**
   - Съединяване на два DataFrame по общ ключ:
     ```python
     df1 = pd.DataFrame({'ID': [1, 2, 3], 'Product': ['Apples', 'Oranges', 'Pears']})
     df2 = pd.DataFrame({'ID': [1, 2, 4], 'Price': [1.20, 2.50, 3.50]})
     result = pd.merge(df1, df2, on='ID', how='inner')
     print(result)
     ```
   - **Таблица след съединение:**
     | ID | Product | Price |
     |----|---------|-------|
     | 1  | Apples  | 1.20  |
     | 2  | Oranges | 2.50  |

2. **Обединение на данни с `concat()`:**
   - Обединяване на списъци от DataFrame-и:
     ```python
     result = pd.concat([df1, df2], ignore_index=True)
     print(result)
     ```

---

## Урок 9: Времеви серии и дата/час операции

### Цели на урока:
- Работа и манипулация на времеви данни в Pandas.

### Стъпки:
1. **Конвертиране на колони във формат `datetime`:**
   - Преобразуване на текстови данни в дата/час:
     ```python
     df['Date'] = pd.to_datetime(df['Date'])
     ```
   - Работа с `resample()` за агрегация по време:
     ```python
     df.set_index('Date', inplace=True)
     resampled = df.resample('M').mean()
     print(resampled)
     ```

---

## Урок 10: Изводи и изготвяне на отчети

### Цели на урока:
- Създаване на сумарни отчети и извличане на аналитични изводи от данните.

### Стъпки:
1. **Създаване на сумарни таблици:**
   - Използване на `pivot_table()` за анализ на данни:
     ```python
     summary = df.pivot_table(values='Age', index='City', aggfunc='mean')
     print(summary)
     ```
   - **Сумарна таблица:**
     | City     | Average Age |
     |----------|-------------|
     | Berlin   | 34          |
     | London   | 42          |
     | New York | 28          |
     | Paris    | 22          |

2. **Визуализация на данни:**
   - Използване на `plot()` за създаване на графики:
     ```python
     summary.plot(kind='bar')
     plt.show()
     ```
## Урок 12: Оптимизация на производителността в Pandas

### Цели на урока:
- Разучаване на методи за подобряване на производителността при работа с големи обеми данни.

### Теоретичен обзор:
Оптимизацията на производителността е критична при анализ на големи датасети. Pandas предоставя няколко инструмента за оптимизация, включително типове данни категории и ускоряващи инструменти като `eval()` и `query()`, които могат да намалят времето за изчисление и употребата на памет.

### Стъпки:
1. **Използване на Categorical данни:**
   - Преобразуване на текстови колони в категорийни, за да намалите употребата на памет:
     ```python
     df['Category'] = df['Category'].astype('category')
     ```

2. **Ускоряване на операции с `eval()` и `query()`:**
   - Използване на `eval()` за бързи математически операции:
     ```python
     df.eval('Total = A + B + C', inplace=True)
     ```
   - Филтриране с `query()`, което е по-бързо от традиционните методи:
     ```python
     result = df.query('Total > 100')
     ```

### Практически примери:
- **Таблица преди и след оптимизация:**
  | ID | Category | A  | B  | C  | Total |
  |----|----------|----|----|----|-------|
  | 1  | Cat1     | 10 | 20 | 30 | 60    |
  | 2  | Cat2     | 20 | 30 | 50 | 100   |
  | 3  | Cat3     | 30 | 40 | 50 | 120   |

- После оптимизация, `Category` колоната използва по-малко памет и заявките са по-бързи.

---

## Урок 13: Сложни филтрации и трансформации

### Цели на урока:
- Разбиране и прилагане на сложни филтрационни и трансформационни методи в Pandas.

### Теоретичен обзор:
Сложните филтрации и трансформации са важни за обработката на данни, които изискват условни логики и преобразувания. Използването на ламбда функции и методите `transform()` и `applymap()` позволява гъвкавост при обработката и е съществено за извличане на полезни аналитични данни.

### Стъпки:
1. **Филтрация с множество условия:**
   - Приложение на сложни логически условия за извличане на подмножества от данни:
     ```python
     filtered = df[(df['A'] > 10) & (df['B'] < 50)]
     ```

2. **Трансформация на данни:**
   - Използване на `applymap()` за прилагане на функция към всяка стойност в DataFrame:
     ```python
     transformed = df.applymap(lambda x: x * 10 if x < 100 else x)
     ```

### Практически примери:
- **Таблица след сложни филтрации и трансформации:**
  | ID | A   | B   | C   |
  |----|-----|-----|-----|
  | 1  | 100 | 200 | 300 |
  | 2  | 200 | 300 | 500 |
  | 3  | 300 | 400 | 500 |

- Примерите илюстрират как данните могат да бъдат модифицирани за по-специфичен анализ или представяне.

---

## Урок 14: Сложни SQL-стил трансформации в Pandas

### Цели на урока:
- Овладяване на сложни SQL-стил трансформации в Pandas, включително оконни функции и динамично преформатиране на данните.

### Теоретичен обзор:
Pandas предлага мощни инструменти за извършване на операции, сходни с тези в SQL, включително оконни функции и динамични преформатирания чрез `pivot()` и `melt()`. Тези инструменти могат да бъдат използвани за създаване на сложни агрегации и за преформатиране на данни за специализирани анализи.

### Стъпки:
1. **Оконни функции:**
   - Използване на `expanding()` за изчисляване на кумулативни суми:
     ```python
     df['Cumulative Total'] = df['Sales'].expanding().sum()
     ```

2. **Динамично преформатиране на данни:**
   - Преобразуване на данни с `pivot()` за създаване на таблици с агрегирани стойности:
     ```python
     pivot = df.pivot(index='Date', columns='Category', values='Sales')
     ```
   - Използване на `melt()` за обратното преобразуване:
     ```python
     melted = pivot.melt(value_vars=['Category'], var_name='Category', value_name='Sales')
     ```

### Практически примери:
- **Таблица след оконни функции и преформатиране:**
  | Date       | Category | Sales | Cumulative Total |
  |------------|----------|-------|------------------|
  | 2021-01-01 | Cat1     | 100   | 100              |
  | 2021-01-02 | Cat2     | 150   | 250              |
  | 2021-01-03 | Cat1     | 200   | 450              |

- Тези примери демонстрират как сложни SQL-стил трансформации могат да се прилагат в Pandas, улеснявайки анализа на данни.

---
## Урок 15: Оптимизация на изпълнението на кода в Pandas

### Цели на урока:
- Изучаване на техники за оптимизация на изпълнението на кода, за да се подобри бързината и ефективността при работа с големи датасети.

### Теоретичен обзор:
Оптимизацията на изпълнението в Pandas е критична за ефективната обработка на големи обеми данни. Техники като профилиране на кода, употреба на Cython или Numba и внимателната управа на паметта могат да намалят значително времето за изчисление.

### Стъпки:
1. **Профилиране на кода:**
   - Използване на Python модули за профилиране за идентификация на бавни части в кода:
     ```python
     import cProfile
     cProfile.run('df.apply(complex_operation)')
     ```

2. **Ускоряване на изчисления с Cython и Numba:**
   - Прилагане на Cython или Numba за компилиране на части от кода, което ускорява изпълнението:
     ```python
     import numba
     @numba.jit
     def fast_operation(x):
         return x * x
     df['squared'] = df['values'].apply(fast_operation)
     ```

### Практически примери:
- **Диаграма на профилиране:**
  Показване на времето за изпълнение и ресурсите, използвани от различни части на кода.

- **Таблица след прилагане на ускорение:**
  | ID | Values | Squared |
  |----|--------|---------|
  | 1  | 10     | 100     |
  | 2  | 20     | 400     |
  | 3  | 30     | 900     |

---

## Урок 16: Работа с текстови данни

### Цели на урока:
- Овладяване на техники за манипулиране на текстови данни в Pandas, включително чистене на текст, използване на регулярни изрази и оптимизиране на текстови операции.

### Теоретичен обзор:
Текстовите данни често изискват специфични методи за предварителна обработка преди анализ. Pandas предлага множество вградени функции за работа с текст, които помагат за нормализация, разделяне на текст и извличане на информация.

### Стъпки:
1. **Нормализация на текст:**
   - Прилагане на низходящ регистър и премахване на пунктуация:
     ```python
     df['Text'] = df['Text'].str.lower().str.replace('[^\w\s]', '')
     ```

2. **Филтрация с регулярни изрази:**
   - Използване на регулярни изрази за извличане на специфични шаблони:
     ```python
     df['Email'] = df['Text'].str.extract('(\\S+@\\S+)')
     ```

### Практически примери:
- **Таблица след текстова обработка:**
  | ID | Text                     | Email           |
  |----|--------------------------|-----------------|
  | 1  | example emailcom         | email@com       |
  | 2  | another testemailcom     | test@email.com  |
  | 3  | sample data noreplycom   | noreply@com     |

---

## Урок 17: Визуализация на данни с Pandas

### Цели на урока:
- Разучаване на методите за визуализация на данни директно чрез Pandas, което улеснява разбирането на данните и представянето на информацията.

### Теоретичен обзор:
Визуализацията е ключов компонент при анализа на данни, тъй като позволява бързо визуално разпознаване на тенденции, аномалии и шаблони. Pandas интегрира тясно с Matplotlib за предоставяне на широк спектър от опции за графично представяне.

### Стъпки:
1. **Линейни графики:**
   - Създаване на линейна графика за показване на тенденции във времето:
     ```python
     df['Sales'].plot(title='Sales Over Time')
     ```

2. **Стълбови диаграми и хистограми:**
   - Използване на стълбови диаграми за сравнение на категорийни данни:
     ```python
     df.plot(kind='bar', title='Comparison of Categories')
     df['Values'].plot(kind='hist', bins=10, title='Distribution of Values')
     ```

### Практически примери:
- **Графика на продажбите през времето и стълбова диаграма за сравнение на категории.**

---

## Урок 18: Работа с времеви данни

### Цели на урока:
- Детайлно разглеждане на функционалности свързани с времеви данни в Pandas, включително парсиране на дати, ресемплиране и създаване на времеви серии.

### Теоретичен обзор:
Времевите данни са често срещан аспект в много анализи, изискващи специално внимание за точността и формата. Работата с времеви серии в Pandas е изключително мощна, като позволява лесно ресемплиране, сдвиг и прозоречни операции.

### Стъпки:
1. **Парсиране и форматиране на времеви данни:**
   - Преобразуване на текстови данни в `datetime` обекти и настройка на формата:
     ```python
     df['Date'] = pd.to_datetime(df['Date'], format='%Y-%m-%d')
     ```

2. **Ресемплиране и агрегиране на времеви серии:**
   - Агрегиране на данни на месечна база и изчисляване на средни стойности:
     ```python
     monthly_data = df.resample('M', on='Date').mean()
     ```

### Практически примери:
- **Таблица след ресемплиране:**
  | Date       | Sales |
  |------------|-------|
  | 2021-01-31 | 150   |
  | 2021-02-28 | 180   |
  | 2021-03-31 | 200   |

---

## Урок 19: Работа с пространствени данни

### Цели на урока:
- Въведение и разглеждане на основите за работа с пространствени данни чрез GeoPandas, като се разгледа интеграцията между GeoPandas и Pandas.

### Теоретичен обзор:
Пространствените данни изискват специални методи за анализ и визуализация. GeoPandas е разширение на Pandas, което предоставя допълнителни възможности за работа с географски данни, като геометрични операции, пространствено присъединяване и визуализации.

### Стъпки:
1. **Създаване на GeoDataFrame:**
   - Импортиране на GeoPandas и конвертиране на DataFrame в GeoDataFrame:
     ```python
     import geopandas as gpd
     gdf = gpd.GeoDataFrame(df, geometry=gpd.points_from_xy(df['Longitude'], df['Latitude']))
     ```

2. **Пространствено присъединяване и анализ:**
   - Използване на пространствено присъединяване за комбиниране на данни на основа на географски местоположения:
     ```python
     merged_data = gpd.sjoin(gdf, other_gdf, op='intersects')
     ```

### Практически примери:
- **Карта с обозначени местоположения и резултати от пространственото присъединяване.**

---

## Урок 20: Безопасност и управление на данни

### Цели на урока:
- Разглеждане на стратегии и техники за осигуряване на безопасността и управлението на данни, включително шифроване, управление на достъпа и безопасно съхранение.

### Теоретичен обзор:
Управлението на данни включва различни аспекти като безопасност, конфиденциалност и интегритет. Пандас предоставя инструменти за управление на достъпа до данни, докато външни библиотеки могат да се използват за шифроване и защита на чувствителна информация.

### Стъпки:
1. **Настройка на роли и права за достъп:**
   - Конфигуриране на правила за достъп до определени части от данните:
     ```python
     # Примерен код за настройка на роли и права за достъп
     ```

2. **Шифроване и безопасно съхранение на данни:**
   - Използване на библиотеки за шифроване за защита на данните:
     ```python
     from cryptography.fernet import Fernet
     key = Fernet.generate_key()
     cipher_suite = Fernet(key)
     df['Encrypted'] = [cipher_suite.encrypt(bytes(x, 'utf-8')) for x in df['Sensitive']]
     ```

### Практически примери:
- **Таблица със зашифровани стойности, показваща как чувствителната информация е защитена.**

---


# ProCredit Bank Test Dashboard
## Опис проєкту
Дашборд побудований в Power BI для аналізу продажів компанії за період 2018–2024 років. Дашборд дозволяє відстежувати ключові метрики, аналізувати продажі за категоріями, країнами та каналами збуту.

![Dashboard Screenshot](https://github.com/tkachukanna/procredit_test_dashboard/blob/main/dashboard.png?raw=true)

### Під час створення дашборду було реалізовано наступні метрики у DAX:

1. Total Sales = SUM(FactSales[SalesAmount]) - загальна сума продажів
2. Total Quantity = SUM(FactSales[Quantity]) - загальна кількість проданих одиниць товару
4. Avg Sales per Order = DIVIDE([Total Sales], DISTINCTCOUNT(FactSales[SalesKey])) - середня сума продажів
5. Total Profit = SUM(FactSales[Profit]) - загальний прибуток
6. Profit Margin % = DIVIDE([Total Profit], [Total Sales]) - відсоток прибутку від загального обсягу продажів

### Візуалізації 

1. KPI Cards - для візуалізації ключових метрик
2. Filled Map - Total Sales by Country
3. Horizontal Bar Chart - Total Sales by Product Category (з drill-down ієрархією: Category → SubCategory)
4. Line Chart - Total Sales by Year and Month (з лінією середнього значення та drill-down ієрархією: Year → Month)
5. Donut Chart - Total Sales by Channel

### Фільтри
- Year - фільтрація по роках 
- Category - фільтрація по категорії продуктів
- Country - фільтрація по країні

### Приклади роботи фільтрів

Продажі для 2024 для США:
![Dashboard Screenshot](https://github.com/tkachukanna/procredit_test_dashboard/blob/main/dashboard_for_2024_usa.png?raw=true)

Продажі за весь час для категорії Clothing:
![Dashboard Screenshot](https://github.com/tkachukanna/procredit_test_dashboard/blob/main/dashboard_for_clothing_category.png?raw=true)


## Ключові інсайти

### Загальні показники
Загальний обсяг продажів за 2018–2024 становить $70.6M при прибутковості 35.6%, що вказує на стабільний показник маржинальності

### Географія продажів
Найвищі продажі зосереджені в Єгипті, Німеччині та ОАЕ - це ключові ринки на які варто робити акцент у стратегії розвитку

### Категорії продуктів
Clothing є лідером продажів, що свідчить про високий попит у цьому сегменті
Furniture показує найменші продажі - варто дослідити причини: низький попит, висока конкуренція або недостатнє просування

### Динаміка продажів
Продажі залишаються стабільними протягом 2018–2024 без явного тренду зростання або спадання
Наявні щомісячні коливання, проте середній рівень тримається стабільно біля лінії середнього значення

### Канали збуту
Всі чотири канали (Online, Retail, Phone, Partner) розподілені майже рівномірно (~25% кожен), тобто продажі не залежать від одного каналу, що знижує ризики

# **README - Sales Analysis Project with Power BI**

## **Project: Comprehensive Sales Analysis System**

### **Project Information**
- **Title:** Python Data Analysis - Power BI
- **Repository:** ANALISIS-DE-DATOS-PYTHON-FO...
- **Data Source:** Business sales dataset
- **Tools:** Python, PostgreSQL, Power BI
- **Status:** Completed

---

## **Project Structure**

### **Main Folders**

```
ANALISIS-DE-DATOS-PYTHON-FO.../
│
├── HU1/                            # User Story 1: Data Import
│   └── sales.ipynb                # Import and initial exploration notebook
│
├── HU2/                            # User Story 2: Cleaning and Normalization
│   └── cleaning_normalization.ipynb  # Data processing and cleaning
│
├── HU3/                            # User Story 3: Data Visualization
│   └── data_visualization.ipynb   # Exploratory visualization with Python
│
├── venv/                          # Python virtual environment
│   ├── Include/
│   ├── Lib/
│   ├── Scripts/
│   ├── share/
│   └── pyvenv.cfg
│
├── Dashboard.pbix             # Main Power BI file
├── DDL.sql                    # SQL script for table creation
├── LICENSE                    # Project license
├── README.md                  # This file
├── requirements.txt           # Project dependencies
├── Star-ER-Model.png         # Data model diagram
├── .env                      # Environment variables
└── .gitignore                # Git ignored files
```

---

## **File Descriptions**

### **1. User Stories (HU)**

#### **HU1: Data Import**
- **File:** `HU1/sales.ipynb`
- **Objective:** Import dataset from Google Drive and perform initial exploration
- **Content:**
  - Google Drive connection
  - CSV file loading (password protected)
  - Initial exploratory analysis
  - Data quality issue identification

#### **HU2: Cleaning and Normalization**
- **File:** `HU2/cleaning_normalization.ipynb`
- **Objective:** Data cleaning, transformation, and preparation for analysis
- **Content:**
  - Null value treatment
  - Format normalization
  - Dimension and fact table creation
  - Preparation for PostgreSQL loading

#### **HU3: Exploratory Visualization**
- **File:** `HU3/data_visualization.ipynb`
- **Objective:** Exploratory analysis and visualization with Python
- **Content:**
  - Distribution charts
  - Temporal analysis
  - Category segmentation
  - Pattern and trend identification

### **2. Configuration and Script Files**

#### **Dashboard.pbix**
- **Type:** Power BI file
- **Description:** Complete interactive dashboard with all visualizations
- **Content:**
  - 4 advanced visualizations
  - Dynamic slicers
  - Monthly sales KPIs
  - Choropleth map by region
  - Top 5 products and clients

#### **DDL.sql**
- **Type:** SQL script
- **Description:** Database schema creation in PostgreSQL
- **Content:**
  - Table creation for all entities
  - Primary and foreign key definitions
  - Index creation for optimization
  - Data type definitions

#### **requirements.txt**
- **Type:** Text file
- **Description:** Python dependencies required for the project
- **Example content:**
  ```
  pandas==2.1.0
  numpy==1.24.0
  matplotlib==3.7.0
  seaborn==0.12.0
  sqlalchemy==2.0.0
  psycopg2-binary==2.9.0
  python-dotenv==1.0.0
  jupyter==1.0.0
  ```

#### **Star-ER-Model.png**
- **Type:** Image file
- **Description:** Star schema data model diagram
- **Model structure:**
  - Fact table: sales_fact
  - Dimension tables: city, product, client_type, product_type, sales_type

#### **.env**
- **Type:** Environment file
- **Description:** Environment variables for database connections
- **Content:**
  ```
  DB_HOST=localhost
  DB_PORT=5432
  DB_NAME=sales_analysis
  DB_USER=postgres
  DB_PASSWORD=your_password
  GOOGLE_DRIVE_URL=https://drive.google.com/file/d/...
  DATA_PASSWORD=R1w1B4q
  ```

---

## **Project Development Process**

### **Phase 1: Data Preparation**
1. **Data Extraction:** Import from Google Drive (password: R1w1B4q)
2. **Data Cleaning:** Handle missing values, correct formats, normalize data
3. **Data Transformation:** Create star schema structure
4. **Database Loading:** Import to PostgreSQL

### **Phase 2: Data Modeling**
1. **Star Schema Design:** Fact and dimension tables
2. **Relationship Definition:** Primary and foreign keys
3. **Performance Optimization:** Index creation
4. **Date Table Creation:** Complete calendar for temporal analysis

### **Phase 3: Analysis and Visualization**
1. **Exploratory Analysis:** Python visualizations
2. **Dashboard Creation:** Power BI with advanced visuals
3. **KPI Definition:** Business metrics calculation
4. **Interactivity Implementation:** Dynamic filters and slicers

---

## **Technical Specifications**

### **Database Schema**
```
1. sales_fact (fact table)
   - sale_id (PK)
   - date_id (FK to calendar)
   - city_id (FK)
   - product_id (FK)
   - client_type_id (FK)
   - sales_type_id (FK)
   - quantity
   - unit_price
   - discount
   - shipping_cost
   - total_sale

2. city_dim (dimension)
   - city_id (PK)
   - city_name

3. product_dim (dimension)
   - product_id (PK)
   - product_name
   - product_type_id (FK)

4. product_type_dim (dimension)
   - product_type_id (PK)
   - product_type

5. client_type_dim (dimension)
   - client_type_id (PK)
   - client_type

6. sales_type_dim (dimension)
   - sales_type_id (PK)
   - sales_type

7. calendar_dim (dimension)
   - date_id (PK)
   - full_date
   - year
   - month
   - month_name
   - day
   - day_of_week
   - week_number
```

### **DAX Measures Implemented**
1. **Sales Comparisons:**
   - Year-over-year sales
   - Month-over-month growth
   - Sales vs previous period

2. **Top Analysis:**
   - Top 5 products by sales
   - Top 5 clients by purchase volume
   - Top cities by revenue

3. **Geographic Analysis:**
   - Sales by city/region
   - Choropleth map visualization
   - Regional performance comparison

4. **Monthly KPIs:**
   - Current month sales
   - Monthly growth rate
   - Year-to-date accumulation
   - Daily average sales

---

## **Power BI Dashboard Features**

### **Visualizations Included**
1. **Sales Comparison:** Current year vs previous year (line chart)
2. **Top Products:** Horizontal bar chart with product categories
3. **Top Clients:** Table with purchase metrics
4. **Choropleth Map:** Geographic sales distribution
5. **Monthly KPIs:** Card visuals with key metrics
6. **Sales Trend:** Time series analysis

### **Interactive Elements**
- **Dynamic Slicers:** Date range, client type, product category, city
- **Cross-filtering:** Click on any visual to filter others
- **Drill-through:** Detailed views from summary metrics
- **Tooltips:** Additional information on hover

### **Filters Applied**
1. **Time Period:** Year, quarter, month, date range
2. **Geography:** City, region selection
3. **Products:** Product type, specific products
4. **Clients:** Client type segmentation

---

## **Setup Instructions**

### **Prerequisites**
1. **Python 3.9+**
2. **PostgreSQL 14+**
3. **Power BI Desktop**
4. **Jupyter Notebook**

### **Installation Steps**
1. Clone the repository:
   ```bash
   git clone [repository-url]
   cd ANALISIS-DE-DATOS-PYTHON-FO...
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # Linux/Mac:
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure database connection in `.env` file

5. Run the notebooks in order:
   ```bash
   jupyter notebook HU1/sales.ipynb
   # Then HU2/cleaning_normalization.ipynb
   # Then HU3/data_visualization.ipynb
   ```

6. Execute SQL script to create database schema:
   ```bash
   psql -U postgres -d sales_analysis -f DDL.sql
   ```

7. Open Power BI Dashboard:
   - Open `Dashboard.pbix` in Power BI Desktop
   - Configure data source connections
   - Refresh data

---

## **Data Source Information**

### **Original Dataset**
- **File:** CSV format
- **Size:** [Specify size]
- **Records:** [Number of records]
- **Source:** Google Drive
- **Access URL:** https://drive.google.com/file/d/11bKrDiC80YP6HNm4v8WpYI8HDPxWVEVt/view
- **Password:** R1w1B4q

### **Data Dictionary**
| Column | Type | Description |
|--------|------|-------------|
| sale_id | Integer | Unique sale identifier |
| date | Date | Sale date |
| city_id | Integer | City identifier |
| product_id | Integer | Product identifier |
| client_type_id | Integer | Client type identifier |
| sales_type_id | Integer | Sale type identifier |
| quantity | Integer | Quantity sold |
| unit_price | Decimal | Price per unit |
| discount | Decimal | Applied discount |
| shipping_cost | Decimal | Shipping cost |
| total_sale | Decimal | Total sale amount |

---

## **User Stories Implementation**

### **HU1: Data Import (Completed)**
- Import from Google Drive with password authentication
- Initial data exploration
- Data quality assessment

### **HU2: Data Transformation (Completed)**
- Null value treatment
- Data type conversion
- Normalization process
- Star schema creation

### **HU3: Python Visualization (Completed)**
- Exploratory data analysis
- Statistical summaries
- Pattern identification
- Preliminary insights

### **HU4: Data Modeling (Completed)**
- PostgreSQL database setup
- Table creation and relationships
- Data loading
- Performance optimization

### **HU5: Power BI Dashboard (Completed)**
- Interactive dashboard creation
- Advanced visualizations
- Dynamic filters implementation
- Documentation and publication

---

## **Key Features**

1. **Comprehensive ETL Pipeline:** End-to-end data processing
2. **Scalable Data Model:** Star schema for analytical queries
3. **Interactive Visualizations:** Business user-friendly interface
4. **Performance Optimized:** Efficient queries and data refresh
5. **Documentation Complete:** All processes documented

---


## **License**

This project is licensed under the MIT License - see the LICENSE file for details.

---

# Brazilian Company and Their Stocks

This is the README file for the dataset representing the Brazilian companies and their stocks along with other features like the legal nature of the company, owner_qualifications and the size of the company.

## Folder Structure
root
 |
 | -> data
 |     |
 |     | -> companies.csv
 |     | -> legal_nature.csv
 |     | -> qualifications.csv
 |     | -> size.csv
 |
 | -> eda.ipynb
 | -> README.md

## File description

data/companies.csv - the actual dataset of companies with other features and the capital_stock
data/legal_nature.csv - records of the different type of the legal_natures a company can have
data/qualifications.csv - records of the different types of qualifications the owner can have
data/size.csv - records of the different type of size the companies are categorised in

eda.ipynb - the python notebook which perform exploratory data analysis on the given dataset

README.md - the file for guidance regarding this small project, navigation for it, and documentation of what was performed in this project

## Data Dictionary
## 📖 Data Dictionary

### companies.csv

| Variable              | Type       | Description                                                                 |
|----------------------|-----------|-----------------------------------------------------------------------------|
| `company_id`          | integer   | Company identifier (8-digit primary key).                                   |
| `company_name`        | string    | Company legal name as provided in the registry.                             |
| `legal_nature`        | string    | Company legal nature (e.g., “Limited Liability Business Company (LLC)”).   |
| `owner_qualification` | string    | Owner/partner qualification label (e.g., “Managing Partner / Partner-Administrator”). |
| `capital_stock`       | numeric   | Declared share capital (BRL).                                               |
| `company_size`        | string    | Company size category (e.g., micro-enterprise, small-enterprise, other).   |

### legal_nature.csv

| Variable       | Type     | Description                                         |
|----------------|---------|-----------------------------------------------------|
| `id`           | integer | Legal nature code (source registry code).          |
| `legal_nature` | string  | Legal nature label corresponding to `id`.         |

### qualifications.csv

| Variable             | Type     | Description                                         |
|---------------------|---------|-----------------------------------------------------|
| `id`                 | integer | Owner qualification code (source registry code).  |
| `owner_qualification`| string  | Owner qualification label corresponding to `id`.  |

### size.csv

| Variable       | Type     | Description                                         |
|----------------|---------|-----------------------------------------------------|
| `id`           | integer | Company size code (source registry code).          |
| `company_size` | string  | Company size label corresponding to `id` (e.g., micro-enterprise, small-enterprise). |

## Data Cleaning & Preparation
Steps performed:

1. **Loaded datasets** using `pandas`.  
2. **Checked for missing values** and data types.  
3. **Verified uniqueness** of `company_id`.  
4. **Merged reference tables** (`legal_nature`, `qualifications`, `size`) with the main dataset, converting categorical columns to IDs.  
5. **Dropped redundant columns** after merging and renamed for clarity (e.g., `legal_nature_id`, `owner_qualification_id`, `company_size_id`).  

## Exploratory Data Analysis (EDA)

### 1. Distribution Analysis
- **Legal Nature**: Bar chart showing the distribution of company legal types.  
- **Owner Qualification**: Bar chart showing the count of companies by owner education/qualification.  
- **Company Size**: Bar chart showing the distribution of small, medium, and large companies.  

### 2. Capital Stock Analysis
- **By Legal Nature**:
  - Calculated average and maximum capital stock for each legal nature.
  - Visualized using a bar chart (linear and log scale) with scatter points for max values.
  
- **By Company Size**:
  - Calculated average and maximum capital stock by company size.
  - Visualized using a log-scaled bar and scatter plot with annotations for better interpretability.
  
- **By Owner Qualification**:
  - Calculated average capital stock for each qualification.
  - Sorted in descending order to highlight top-performing owner qualifications.

### 3. Top Capital Companies
- Filtered the **top 25% of companies by capital stock**.
- Analyzed their distribution across legal nature, owner qualifications, and company sizes.  
- Visualized company size distribution among top-capital companies.

## Key Findings
1. Certain **legal natures** consistently have higher average and maximum capital stocks.  
2. Companies owned by individuals with specific **qualifications** tend to have higher capital stock.  
3. Larger companies dominate the top 25% of capital stock distribution, but exceptions exist across other categories.  

## Visualizations
The project includes clear visualizations to communicate patterns:

- Bar charts for distributions (legal nature, owner qualification, company size)  
- Comparative bar & scatter plots for average vs max capital stock by category  
- Log-scaled charts for skewed capital stock distributions  
- Annotated bars and scatter points for clarity  

## Libraries Used
- `pandas` for data manipulation  
- `numpy` for numerical operations  
- `matplotlib` for plotting and visualization  

## How to Run
1. Clone the repository and place all datasets in the `data/` folder.  
2. Run the Python script or Jupyter notebook in order.  
3. Ensure required libraries are installed:

```bash
pip install pandas numpy matplotlib
```



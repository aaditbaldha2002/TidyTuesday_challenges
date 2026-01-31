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




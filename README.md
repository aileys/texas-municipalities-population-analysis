# Analysis of Municipalities in Texas

This project collects, cleans, and analyzes population data for Texas municipalities using data scraped from the Wikipedia page **"List of municipalities in Texas"**. I use Python to build a reproducible pipeline that downloads the data, stores it in CSV files, and generates basic descriptive statistics and visualizations.

## Project Goals

- Practice web scraping with `requests`, `BeautifulSoup`, and `wikipedia-api`
- Clean and structure semi-structured HTML table data into a tidy DataFrame
- Explore population trends and rankings for Texas cities and towns
- Generate summary statistics and visualizations of 2020–2023 population estimates

## Data

The data is sourced from the Wikipedia page “List of municipalities in Texas” and processed into two CSV files:

- `data/raw_texas_cities.csv` – original scraped table values
- `data/texas_cities.csv` – cleaned dataset with:
  - **2023 Rank** – rank based on population
  - **Municipality** – city/town name
  - **Designation** – city, town, or village
  - **Primary County** – primary county for the municipality
  - **2023 Estimate** – estimated 2023 population
  - **2020 Census** – population from the 2020 U.S. Census

> Note: The CSV files included here are for demonstration and coursework. For the most up-to-date figures, refer to the original Wikipedia page and official census data.

## Methods

Key steps implemented in the notebook:

1. **Web Scraping**
   - Send HTTP requests to the Wikipedia URL
   - Parse HTML with `BeautifulSoup`
   - Extract headers and row values from the target table

2. **Data Cleaning**
   - Remove non-numeric characters from population columns
   - Convert population fields to integers
   - Handle missing values and drop irrelevant rows
   - Save both raw and cleaned data as CSV files

3. **Exploratory Data Analysis**
   - Use `pandas.DataFrame.describe()` to summarize population metrics
   - Sort cities by 2023 estimated population and census counts
   - Identify largest municipalities by rank and growth

4. **Data Visualization**
   - Bar charts of the top 10 municipalities by 2023 estimated population
   - (Optional) additional plots showing distribution of population or changes over time

## Technologies Used

- **Language:** Python
- **Libraries:**
  - `requests`
  - `beautifulsoup4`
  - `wikipedia-api`
  - `pandas`
  - `matplotlib`
  - `seaborn`
- **Tools:** Jupyter Notebook / Google Colab

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/texas-municipalities-population-analysis.git
   cd texas-municipalities-population-analysis


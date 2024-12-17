# Indeed Job Scraper  

## Project Overview  

This project is a **web scraper** designed to extract job postings from **Indeed.com**. It gathers information about job titles, company names, locations, and descriptions for software developer roles in New York and saves the data to a CSV file. This script is a simple way to automate the collection of job listings for further analysis.

---

## Features  

1. **Extract Job Data**  
   - Scrapes job title, company, location, and job description from Indeed listings.  

2. **Save to CSV**  
   - Stores the extracted data in a neatly formatted CSV file with a timestamp.  

3. **Easy Configuration**  
   - Change the URL to search for different job roles or locations.  

4. **Data Analysis Ready**  
   - The saved CSV file can be imported into tools like Excel, Python Pandas, or Power BI for analysis.  

---

## Table of Contents  

1. [Installation](#installation)  
2. [Project Structure](#project-structure)  
3. [Dependencies](#dependencies)  
4. [How It Works](#how-it-works)  
5. [Usage](#usage)  
6. [Customization](#customization)  
7. [Limitations](#limitations)  
8. [Future Improvements](#future-improvements)  

---

## Installation  

Follow these steps to set up and run the project:

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/job-scraper.git
   cd job-scraper
   ```

2. **Install Required Libraries**  
   Use `pip` to install the necessary Python libraries:  
   ```bash
   pip install requests beautifulsoup4
   ```

3. **Run the Script**  
   Execute the script to scrape jobs and save them to a CSV file:  
   ```bash
   python scraper.py
   ```

---

## Project Structure  

The project consists of a single Python script:  

```bash
├── job_scraper.py    # The main script for scraping and saving job data
└── README.md         # Project documentation
```

---

## Dependencies  

The script relies on the following Python libraries:

| Library           | Description                                      |
|--------------------|-------------------------------------------------|
| `requests`        | Sends HTTP requests to fetch the web page.       |
| `beautifulsoup4`  | Parses the HTML content of the web page.         |
| `csv`             | Saves the extracted data into a CSV file.        |
| `datetime`        | Generates a timestamp to create unique filenames.|

Install all dependencies using:  
```bash
pip install requests beautifulsoup4
```

---

## How It Works  

1. **HTTP Request**:  
   - The script sends a GET request to the Indeed job search page URL.

2. **HTML Parsing**:  
   - The content of the webpage is parsed using `BeautifulSoup`.

3. **Data Extraction**:  
   - The scraper extracts job titles, company names, locations, and descriptions.  
   - It looks for specific HTML elements (`div`, `h2`, `span`) with relevant classes.

4. **Save to CSV**:  
   - The job data is saved into a CSV file with a unique timestamp in its name.

5. **Output**:  
   - The saved file is displayed in the terminal for easy access.

---

## Usage  

1. Run the script:  
   ```bash
   python job_scraper.py
   ```

2. The program will:  
   - Scrape job listings for **Software Developer** roles in **New York**.  
   - Save the data to a CSV file named like `jobs_YYYY-MM-DD_HHMMSS.csv`.  

3. Open the CSV file in Excel, Google Sheets, or Python for further processing.

---

## Customization  

1. **Change Job Role and Location**:  
   Modify the `url` variable at the top of the script to search for different roles or cities. For example:  
   ```python
   url = 'https://www.indeed.com/jobs?q=data+scientist&l=San+Francisco'
   ```

2. **Add More Fields**:  
   - If you want to extract additional details (like salary, posting date), inspect the HTML structure of the job listings and modify the script accordingly.

3. **Change Output Filename**:  
   - Update the naming convention in the `filename` variable:  
     ```python
     filename = 'job_listings.csv'
     ```

---

## Limitations  

1. **HTML Structure Changes**:  
   - If Indeed updates its HTML structure, the script might fail to extract data correctly.  

2. **Pagination**:  
   - The current script scrapes only the first page of job listings.  

3. **Rate Limiting**:  
   - Frequent requests to the website may trigger rate limiting or blocks. Always scrape responsibly.

4. **Dynamic Content**:  
   - If jobs are loaded dynamically using JavaScript, the script might not capture them. Use tools like Selenium for such cases.

---

## Future Improvements  

- **Pagination Support**: Scrape job listings across multiple pages.  
- **Dynamic Content Handling**: Integrate Selenium or Playwright for JavaScript-rendered content.  
- **Error Handling**: Add robust error handling for missing elements or request failures.  
- **Filter Job Listings**: Allow filtering results based on keywords or companies.  
- **Visualization**: Create visualizations for job data (e.g., top companies hiring, location distribution).  

---

## Acknowledgments  

- **Indeed** for providing job search listings.  
- **BeautifulSoup** for simplifying HTML parsing.  
- **Requests** for HTTP requests.

---

### Happy Job Hunting! 🚀  

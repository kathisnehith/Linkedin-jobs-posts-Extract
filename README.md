# LinkedIn Jobs and Hiring Posts Scraper

This repository contains Python scripts designed for scraping job listings and specific hiring posts from LinkedIn. These scripts automate the retrieval of job information based on user-defined criteria, simplifying the process of filtering and analyzing job opportunities and hiring posts. This reduces the manual analysis time for specific needs, as it's just a matter of filtering through the data sheets to pinpoint accurate details.


## Use-Case
- Recruitment: Quickly gather data on job openings for specific roles to analyze market trends or to prepare targeted recruitment strategies.
- Job Hunting: For individuals looking for jobs, this can automate the process of finding new listings that match their criteria.
- Market Research: Companies can use this to monitor competitors' hiring activities or to understand workforce demand in various sectors.

## Overview

**Linkedin_hirepost_scraper_code.py:**
- **Purpose:** Extracts LinkedIn hiring posts specifically from the LinkedIn search results page based on keywords, location, and posting date.
- **Functionality:** 
  - Logs into LinkedIn using predefined credentials.
  - Searches for posts with specific keywords like "Data Analyst" or "Business Analyst" and "hiring' or 'looking for".
  - Extracts details such as job title, location, company, posting time, and links to the job and company profiles.
  - Saves the collected data into a CSV file named `linkedin_hiringposts.csv`.

**Linkedinjobs_scraper_code.py:**
- **Purpose:** Scrape job listings from LinkedIn based on job titles and locations.
- **Functionality:**
  - Also requires login to LinkedIn with credentials.
  - Searches for jobs across various pages for each job title in each location.
  - Gathers job title, location details, company name, posting date, job link, and company link.
  - Data is then compiled into a pandas DataFrame and saved as `linkedinJobs_data.csv`.

**Note:** The codes are in raw format with hardcoding of the parameters and URLs to extract.
## Usage

### Prerequisites
- Python 3.6+
- `selenium`, `beautifulsoup4`, `pandas`, `requests`, `webdriver-manager`

### Installation
1. Clone the repository:
   ```sh
   git clone [your-repo-url]
   cd [cloned-repo-name]

2. Install the required packages:
   ```sh
   pip install -r requirements.txt

Setup
- Recommended to use the **Windows** operating system for error-free execution.
- Ensure you have the latest version of Chrome and the corresponding ChromeDriver installed. The path to chromedriver.exe should be correctly set in the scripts.
- Replace [email@gmail.com]() and [password]() in both scripts with your LinkedIn credentials. Note: Hardcoding credentials is not secure for production use; consider using environment variables or a secure configuration method in real-world scenarios.

Running the Scripts:
- For Linkedin_hirepost_scraper_code.py:
  ```sh
    python Linkedin_hirepost_scraper_code.py
- For Linkedinjobs_scraper_code.py:
  ```sh
  python Linkedinjobs_scraper_code.py

## Limitations
- **LinkedIn's Terms of Service:** Scraping LinkedIn data might violate their terms. Use this tool for personal, non-commercial use at your own risk.
- **Data Accuracy:** The accuracy of the scraped data depends on LinkedIn's page structure which can change, potentially breaking the scraping logic.

## Future works
- **Airflow Orchestration:** Implement orchestration with Airflow to run both scripts with specific parameters, extracting jobs and posts in one go on a scheduled basis.
- **Keyword-Based Extraction:** Enhance the scripts to extract data only when specific keywords match, automatically filtering results. The data will then be saved to a Google Sheets link, accessible to anyone.


## Sources Used
- **Stack Overflow:** Utilized for solving specific programming challenges and understanding best practices in web scraping with Python.
- **BeautifulSoup Documentation:** Referenced for learning how to parse HTML and XML documents efficiently.
- **HTML Script Documentation:** Studied to understand the structure of web pages and how to effectively target elements for scraping.
- **Open Source HTML Script Scraper Codes:** Reviewed various open-source projects to gather insights and inspiration for implementing scraping functionalities, adapting existing solutions to fit the needs of this project.

## Contributions
Contributions are welcome! If you find bugs or have suggestions for improvements:
Fork the repository
Make your changes
Open a pull request

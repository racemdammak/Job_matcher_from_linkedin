# LinkedIn Job Scraper and Matcher

This project scrapes job postings from LinkedIn based on job title and location, and matches them to a candidate's CV using natural language processing to recommend the best job matches.

## Features

- **Job Scraping**: Scrapes job postings from LinkedIn using web scraping techniques.
- **Job Matching**: Uses sentence embeddings and cosine similarity to match job descriptions with a candidate's CV.
- **Data Storage**: Saves job recommendations to a text file.

## Requirements

- Python 3.7+
- Libraries: requests, beautifulsoup4, pandas, pdfplumber, sentence-transformers, scikit-learn

## Installation

1. Clone the repository or download the files.
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```
   Note: You may need to install additional dependencies like PyTorch for sentence-transformers.

## Usage

### Job Scraping

- Use the `main.ipynb` Jupyter notebook to scrape jobs interactively.
- Or use the `Jobscraping` class in `Jobscraping.py`:
  ```python
  from Jobscraping import Jobscraping
  scraper = Jobscraping()
  jobs = scraper.scrape_jobs("Machine Learning Engineer", "Tunisia")
  ```

### Job Matching

- Run `job_matcher.py` to match jobs to a CV.
- Ensure you have a PDF CV file (currently hardcoded as "racem dammak.pdf").
- The script will output job recommendations sorted by match score and save them to `job_recommendations.txt`.

## Files

- `main.ipynb`: Jupyter notebook for testing job scraping.
- `Jobscraping.py`: Class for scraping LinkedIn jobs.
- `job_matcher.py`: Script for matching jobs to a CV.
- `requirements.txt`: List of required Python packages.

## Notes

- LinkedIn's structure may change, so the scraping selectors might need updates.
- The CV file path is hardcoded; modify as needed.
- This is for educational purposes; respect LinkedIn's terms of service.

## Authors

Yasmine & Racem

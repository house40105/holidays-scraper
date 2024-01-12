# Holidays Scraper  
This Go application is designed to scrape and collect holiday data from the [OfficeHolidays website](https://www.officeholidays.com/). The program fetches holiday information for a specific country and a set of years, processes the data, and generates a CSV file containing the holiday details.
### Table of Contents  

### Introduction
The Holidays Scraper stands as a command-line application meticulously developed in the Go programming language, purposefully designed to automate the extraction of holiday-related information from the OfficeHolidays website. This adept tool strategically utilizes the [Colly](https://github.com/gocolly/colly) library for proficient web scraping, augmenting its capabilities with features including the adept management of compensatory holidays and the incorporation of extended weekends.  

### Features
1. **Web Scraping:** Utilizes the Colly library to navigate through the OfficeHolidays website and extract holiday data.  
2. **Compensatory Holidays:** Identifies and includes compensatory holidays based on specific criteria.
3. **Extended Weekends:** Adds entries for extended weekends (Saturday and Sunday) around public holidays falling on Fridays or Mondays.
4. **CSV Output:** Generates a CSV file with comprehensive holiday details including day, date, holiday name, type, and additional comments.

### Usage
To use the Holidays Scraper, follow these steps:
1. **Install Dependencies:** Make sure you have Go installed on your machine.
2. **Clone the Repository:**
   ```sh
   git clone https://github.com/house40105/holidays-scraper.git
   cd holidays-scraper
   ```
4. 

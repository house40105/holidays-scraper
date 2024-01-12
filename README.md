# Holidays Scraper  
This Go application is designed to scrape and collect holiday data from the [OfficeHolidays website](https://www.officeholidays.com/). The program fetches holiday information for a specific country and a set of years, processes the data, and generates a CSV file containing the holiday details.
### Table of Contents  
- [Introduction](#Introduction)
- [Features]
- [Usage]
- [Installation]
- [Configuration]
- [Dependencies]

### Introduction
The Holidays Scraper stands as a command-line application meticulously developed in the Go programming language, purposefully designed to automate the extraction of holiday-related information from the OfficeHolidays website. This adept tool strategically utilizes the [Colly](https://github.com/gocolly/colly) library for proficient web scraping, augmenting its capabilities with features including the adept management of compensatory holidays and the incorporation of extended weekends.  

### Features
- **Web Scraping:**  
   Utilizes the Colly library to navigate through the OfficeHolidays website and extract holiday data.
- **User-Agent Simulation:**  
  The program simulates a real user by setting a random User-Agent header for each HTTP request.
- **Error Handling:**  
  Comprehensive error handling is implemented to log errors and continue processing other years in case of any issues.
- **Date Parsing:**  
  The program parses date strings from the website and converts them into a consistent format.
- **Compensatory Holidays:**  
   The program detects compensatory holidays embedded in the comments and seamlessly integrates them into the final output. It performs this task with precision, identifying and incorporating compensatory holidays according to specific criteria defined within the system
- **Extended Weekends:**  
   Adds entries for extended weekends (Saturday and Sunday) around public holidays falling on Fridays or Mondays.
- **CSV Output:**  
   Generates a CSV file with comprehensive holiday details including day, date, holiday name, type, and additional comments.

### Usage
To use the Holidays Scraper, follow these steps:
1. **Install Dependencies:**  
   Make sure you have Go installed on your machine.
2. **Clone the Repository:**
   ```sh
   git clone https://github.com/house40105/holidays-scraper.git
   cd holidays-scraper
   ```
3. **Run the Application:**
   ```sh
   go run Holidays_Scraper.go
   ```
4. **Check the Output:**  
   Once the execution is complete, a CSV file named `holiday.csv` will be generated in the project directory containing the holiday data.

### Configuration
The application is configured with the following variables:
- `baseURL`: The base URL for the OfficeHolidays website.
- `country`: The target country for which holiday data is retrieved.
- `optputFileName`: The output filename for the generated CSV file.
- `yearsList`: The list of years for which holiday data is collected.
- `targetDateFormat`: The desired date format for the output.
- `logFormat`: The format for log messages.
These variables can be adjusted in the Holidays_Scraper.go file to customize the scraping behavior.

### Dependencies
The Holidays Scraper relies on the Colly library for web scraping. Ensure that this library is installed using the following command:
```sh
go get -u github.com/gocolly/colly/v2
```

# Holidays Scraper  
This Go application is designed to scrape and collect holiday data from the [OfficeHolidays](https://www.officeholidays.com/) website. The program fetches holiday information for a specific country and a set of years, processes the data, and generates a CSV file containing the holiday details.
### Table of Contents  
- [Introduction](#Introduction)
- [Features](#Features)
- [Usage](#Usage)
- [Configuration](#Configuration)
- [Dependencies](#Dependencies)
- [Execution Results](#Execution-Results)

### Introduction
The Holidays Scraper stands as a command-line application meticulously developed in the Go programming language, purposefully designed to automate the extraction of holiday-related information from the OfficeHolidays website. This adept tool strategically utilizes the [Colly](https://github.com/gocolly/colly) library for proficient web scraping, augmenting its capabilities with features including the adept management of compensatory holidays and the incorporation of extended weekends.  

### Features
- **Web Scraping:** Utilizes the Colly library to navigate through the OfficeHolidays website and extract holiday data.
- **User-Agent Simulation:**  The program simulates a real user by setting a random User-Agent header for each HTTP request.
- **Error Handling:**  Comprehensive error handling is implemented to log errors and continue processing other years in case of any issues.
- **Date Parsing:**  The program parses date strings from the website and converts them into a consistent format.
- **Compensatory Holidays:**  The program detects compensatory holidays embedded in the comments and seamlessly integrates them into the final output. It performs this task with precision, identifying and incorporating compensatory holidays according to specific criteria defined within the system
- **Extended Weekends:**  Adds entries for extended weekends (Saturday and Sunday) around public holidays falling on Fridays or Mondays.
- **CSV Output:**  Generates a CSV file with comprehensive holiday details including day, date, holiday name, type, and additional comments.

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
- `country`: The target country for which holiday data is retrieved.Update this variable with the desired country code.  
- `optputFileName`: The output filename for the generated CSV file.Modify this variable to set the name of the CSV file that will store the holiday data.  
- `yearsList`: The list of years for which holiday data is collected.Add or remove years in this list to specify the range of years for which you want to scrape holiday information.  
- `targetDateFormat`: The desired date format for the output.Adjust this variable to set the format in which the dates will be represented in the generated CSV file.  
- `logFormat`: The format for log messages.  
  
These variables provide flexibility, allowing you to tailor the scraping behavior according to your specific requirements. Update them as needed to achieve the desired configuration for the Holidays Scraper.

### Dependencies
The Holidays Scraper relies on the Colly library for web scraping. Ensure that this library is installed using the following command:
```sh
go get -u github.com/gocolly/colly/v2
```
### Execution Results
After running the Holidays_Scraper.go program, you can expect the following results:  

**Console Output**  
The program provides console output to keep you informed about its progress. The console output includes details such as visited URLs, errors, and other relevant information. Below is an example of what you might see in the console:  
![Console_Output](https://github.com/house40105/holidays-scraper/blob/main/fig/Console_Output.png)

**CSV Output**  
The program generates a CSV file containing the scraped holiday data. The CSV file is named based on the `optputFileName` variable. Here is an example of how the CSV file's content might look:  
```plaintext
Day       Date       Holiday Name              Holiday Type      Is Holiday    Comments
Friday    2024-01-01 New Year's Day            Public Holiday    true          Celebrating the beginning of the new year
Monday    2024-02-12 Chinese New Year          Public Holiday    true          Celebrating the Chinese New Year
...
```

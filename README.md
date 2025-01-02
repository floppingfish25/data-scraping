# Store Location Scraper

## Approach

The goal of this project is to scrape store location data for various brands (CU and McDonald's) and convert the addresses into geographic coordinates (longitude and latitude). The scraper fetches the store names and addresses, and attempts to geocode them using the free Nominatim geocoder from OpenStreetMap. However, due to API limitations and costs associated with Google Maps, there are some challenges in accurately geocoding all addresses.

### Steps:
1. Scrape store location data from the respective websites.
2. Extract the store names and addresses from the pages.
3. Store the extracted data into CSV files.
4. Attempt to convert the extracted addresses into geographic coordinates (longitude and latitude) using the free Nominatim geocoding service.
5. Save the final data, including the coordinates (if available), into a CSV file.

## Tools

- **Selenium**: Used for web scraping by automating browser interaction. Selenium allows navigation of dynamic websites and interact with elements like buttons and dropdowns.
- **Geopy**: A Python library that provides geocoding functionality, used here for converting addresses into longitude and latitude coordinates.

## Known Issues

- **Geocoding**: The free geocoding service (Nominatim) does not always provide accurate results, especially for addresses that are less specific or ambiguous. Additionally, due to the limitations of the free API, not all addresses will successfully be converted into geographic coordinates.
- **Google Maps API Cost**: A more reliable geocoding service, such as the Google Maps API, requires a paid plan and is therefore not used in this project to avoid cost-related constraints.
- **McDonald's Scraping**: The process of scraping McDonald's store locations has been particularly challenging due to the website's dynamic nature and inconsistent HTML structure. This resulted in some difficulties in extracting the necessary data.

## Usage

1. **Install Dependencies**: Ensure you have the required Python libraries installed:
   ```bash
   pip install selenium pandas geopy

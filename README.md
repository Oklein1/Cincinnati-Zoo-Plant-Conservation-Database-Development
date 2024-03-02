# Cincinnati-Zoo-Plant-Conservation-Database-Development


### Project Overview
The Cincinnati Zoo & Botanical Garden, under the leadership of Dr. Valerie Pence, spearheads this collaborative effort to devise effective conservation methods for exceptional plant species. By harnessing digital tools, the project endeavors to build a comprehensive database tailored for conservation practitioners. The database will analyze various factors including media, hormones, and freezing methods concerning different taxa. Additionally, it will integrate environmental adaptation data and amalgamate information from sources such as GBIF and weather stations. This initiative aims to streamline protocol development and enhance predictability in plant conservation efforts, empowering researchers at the Cincinnati Zoo and a broader global network of conservationists dedicated to preserving exceptional plant species worldwide.

### Code Description
The provided Python code offers functionalities to fetch weather data and species occurrences, crucial components for the database development process. Below is a brief description of the main functions:

- **`get_weather(lat, lon, api_key)`**: Retrieves weather data based on latitude and longitude coordinates using the OpenWeatherMap API.

- **`get_species_occurrences(species_name)`**: Fetches species occurrence data from the Global Biodiversity Information Facility (GBIF) API based on the scientific name of the species.

- **`gbif_api_extracter(df)`**: Extracts species occurrences for each species in the provided DataFrame.

- **`build_pandas_df_from_matrix(api_extractor_list)`**: Constructs pandas DataFrames from a list of lists obtained from the GBIF API extractor.

- **`process_data(path)`**: Processes the input data from a CSV file, retrieves species occurrences, and returns a concatenated DataFrame.

- **`main(path)`**: The main function orchestrates the data processing pipeline and can be used as a starting point for further customization.


## Data Sources and APIs

### GBIF API Integration

The project utilizes the Global Biodiversity Information Facility (GBIF) API to retrieve species occurrence data. By interfacing with the GBIF API, we gather valuable information about the distribution and occurrences of plant species. The `get_species_occurrences(species_name)` function queries the GBIF database based on the scientific name of the species provided. This data is then processed to enrich our conservation database, aiding in better understanding the distribution patterns of exceptional plant species.

### Weather Station API Integration

To incorporate environmental factors into our conservation database, we leverage weather data from various weather stations using an external API. The `get_weather(lat, lon, api_key)` function interacts with the OpenWeatherMap API to fetch current weather conditions based on latitude and longitude coordinates. These weather parameters, including temperature, humidity, wind speed, and description, are essential for analyzing the impact of environmental variables on plant species. By integrating weather data, we aim to enhance the accuracy and effectiveness of conservation protocols, providing valuable insights for conservation practitioners.

### Usage Notes

Before running the code, ensure that you have obtained valid API keys for both the GBIF and weather station APIs. Replace the placeholder API keys in the code with your own keys to enable access to these services. Additionally, review the API documentation to understand any usage limits or restrictions imposed by the providers.

### Usage
To utilize the provided code, follow these steps:

1. Ensure you have the necessary dependencies installed, including pandas and requests.
2. Replace placeholder API keys with valid ones for OpenWeatherMap and GBIF APIs.
3. Adjust input paths and parameters as per your requirements.
4. Execute the `main()` function with appropriate arguments to initiate the data processing pipeline.

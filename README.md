# 🦊QueryBot README

## Overview

🦊QueryBot is an interactive Streamlit application designed to enhance your data analysis experience by enabling natural language queries on your CSV files or MySQL database. The application supports data visualization, translation of responses into multiple languages, and even generates audio responses using text-to-speech.

## Features

- **Data Summarization**: Get summaries such as average values, total counts, and unique entries.
- **Data Visualization**: Visualize data over specified periods.
- **Natural Language Queries**: Ask custom questions and get specific answers about your data.
- **Translation**: Translate responses into multiple languages.
- **Text-to-Speech**: Generate and play audio responses.

## Setup

### Prerequisites

- Python 3.8 or higher
- Required Python packages: `streamlit`, `pandas`, `dotenv`, `pandasai`, `matplotlib`, `requests`, `translatepy`, `gtts`, `mysql-connector-python`

### Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/your-repo/querybot.git
   cd querybot
   ```

2. **Install dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root directory and add your `PANDASAI_API_KEY`:
   ```env
   PANDASAI_API_KEY=your_api_key_here
   ```

## Running the Application

Start the Streamlit app by running:
```sh
streamlit run app.py
```

## Usage

1. **Launch the Application**:
   Open your browser and navigate to `http://localhost:8501` (or the URL provided in the terminal).

2. **Select Data Source**:
   Choose between a CSV file or a MySQL database as your data source.

3. **CSV File**:
   - Upload a CSV file.
   - View the uploaded data.
   - Select a column and visualize the data over a specified period.
   - Enter a query to interact with your data.
   - Select a language for the response.
   - Get the translated response and listen to the audio.

4. **MySQL Database**:
   - Enter connection details (host, database, user, password).
   - Execute a query to fetch data.
   - View the fetched data.
   - Select a column and visualize the data over a specified period.
   - Enter a query to interact with your data.
   - Select a language for the response.
   - Get the translated response and listen to the audio.

## Functions

### `check_connectivity()`
Checks for internet connectivity.

### `chat_with_csv(df, prompt)`
Interacts with a DataFrame based on a natural language query.

### `translate_text(text, target_language)`
Translates text to the specified language using `translatepy`.

### `generate_speech(text, lang)`
Generates speech from text using Google Text-to-Speech (gTTS).

### `fetch_data_from_mysql(host, database, user, password, query)`
Fetches data from a MySQL database based on the provided query.

### `visualize_data(df, column_to_plot)`
Visualizes the specified column data over 12 months.

## Dependencies

- `streamlit`: For creating the web app interface.
- `pandas`: For data manipulation.
- `dotenv`: For loading environment variables.
- `pandasai`: For natural language querying of DataFrames.
- `matplotlib`: For data visualization.
- `requests`: For checking internet connectivity.
- `translatepy`: For translating text.
- `gtts`: For generating speech from text.
- `mysql-connector-python`: For connecting to MySQL databases.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.


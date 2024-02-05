# HTML to SQLite Converter

This Python script converts HTML data from multiple URLs containing journal titles and their respective abbreviations into an SQLite database. The script fetches data from specified URLs, processes the HTML content, and stores the extracted journal titles and abbreviations in an SQLite database, facilitating easy access and management of journal information.

## Features

- **Data Extraction:** The script utilizes BeautifulSoup to parse HTML content, extracting journal titles and their corresponding abbreviations from specified URLs.
- **Data Cleaning:** It cleans and processes the extracted data, ensuring uniformity and consistency in the stored information.
- **SQLite Integration:** The script seamlessly integrates with SQLite, providing a lightweight and efficient database solution for storing journal data.
- **Custom Capitalization Logic:** It applies custom capitalization logic to ensure proper capitalization of journal titles, handling exceptions like "of" and "the" to maintain title case format.

## Requirements

- Python 3.x
- BeautifulSoup4
- requests

## Installation

Clone the repository:

```bash
git clone https://github.com/blipovski/html-to-sqlite-converter.git
```

Install the required Python packages:

```bash
pip install beautifulsoup4 requests
```

## Usage

Modify the main function in the converter.py script to adjust the URLs, database name, and other parameters as needed.

Run the script:

```bash
python html-sql.py
```

# Academic Journal Abbreviation Database

The SQLite output file generated by the HTML to SQLite Converter script contains the processed journal titles and their corresponding abbreviations. The database is structured with two columns: title and abbreviation.

## Usage

- **Accessing the SQLite Database:** You can access the SQLite database using any SQLite client or library compatible with your programming language of choice.
- **Querying Data:** Retrieve journal titles and abbreviations by executing SQL queries against the database.
- **Integration with Applications:** Integrate the SQLite database into your applications to access and utilize journal information efficiently.

## Data Source

The data used in this converter is sourced from the [Web of Science Journal Title and Journal Abbreviation Database](https://images.webofknowledge.com/images/help/WOS/A_abrvjt.html). The journal titles and abbreviations are contained within HTML files accessible via separate URLs, organized alphabetically including one url for numerals (0-9).

Credit goes to Web of Science for hosting the valuable dataset.

## File Location

The SQLite output file is created in the same directory where the script is run. The default name of the SQLite database file is `journals.db`, as specified in the script. You can customize the file name and location by modifying the script accordingly.

Feel free to explore and analyze the data stored in the SQLite database to extract valuable insights and information about journal titles and abbreviations.

# License

This project is licensed under the MIT License - see the LICENSE file for details.

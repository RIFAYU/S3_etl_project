
![etl_job drawio](https://github.com/user-attachments/assets/4d89d47f-33cf-4cf3-b6db-a7d5ab4030cf)

# Output of this project
![s1](https://github.com/user-attachments/assets/69443a1b-9895-4752-aa99-de56b9b20629)

From this project, we clearly understood how ETL works :)

# ETL Pipeline for Sales Data

This project is a simple ETL (Extract, Transform, Load) pipeline built in Python that processes sales data stored in JSON format on Amazon S3, transforms it using the `pandas` library, and loads the processed data into a PostgreSQL database for storage and analysis.

### Project Overview

The pipeline follows these steps:

1. **Extract**: Connect to an S3 bucket, retrieve sales data files in JSON format, and load them into a `pandas` DataFrame for transformation.
2. **Transform**: Clean and transform the raw data using `pandas`:
   - Normalize JSON structure and convert it into a tabular format.
   - Format column names and handle missing data.
   - Set appropriate data types to optimize storage and querying.
3. **Load**: Connect to a PostgreSQL database and upload the cleaned data into a designated table using SQLAlchemy and `pandas` methods for efficient data loading.

### Project Features

- **Automated Data Retrieval**: Fetches data directly from an S3 bucket using `boto3`.
- **Data Cleaning & Transformation**: Prepares data for easy analysis, with structured formatting and type assignment.
- **Database Integration**: Loads the final processed data into PostgreSQL, making it accessible for business intelligence and analysis.

### Technologies Used

- **Python**: Main programming language
- **pandas**: Data manipulation and transformation
- **boto3**: S3 data extraction
- **SQLAlchemy & psycopg2**: PostgreSQL connection and data loading

### Prerequisites

- **AWS S3 Access**: Access key and secret key for the S3 bucket containing sales data.
- **PostgreSQL Database**: Connection details for the target PostgreSQL instance.

### Usage

1. Set up AWS credentials and PostgreSQL connection details.
2. Run the ETL script to automatically extract, transform, and load data.

This ETL pipeline is intended for use cases where sales data is updated regularly on S3, enabling efficient and automated data processing and storage for downstream analysis.

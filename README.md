# Aarogya

## Description

Aarogya is a Java-based application designed to manage patient records. It provides functionalities for patient registration, querying patient data, exporting data to a CSV file, and displaying patient information. The application connects to a MySQL database to store and retrieve patient information.

## Features

- **User Authentication**: Simple login mechanism with predefined credentials.
- **Patient Registration**: Register new patients with details such as name, age, sex, address, phone number, etc.
- **Query System**: Execute queries to retrieve specific patient information.
- **Data Export**: Export patient data to a CSV file.
- **Data Display**: Display patient data in a user-friendly GUI.

## Requirements

- **Java Development Kit (JDK)**: Version 8 or higher.
- **MySQL Database**: Ensure MySQL server is running and accessible.
- **Java Database Connectivity (JDBC) Driver**: MySQL Connector/J.

## Setup

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/aarogya.git
    cd aarogya
    ```

2. **Database Setup**:
    - Create a MySQL database named `arogya`.
    - Create a table named `patients` with the following schema:
      ```sql
      CREATE TABLE patients (
          Registration_no VARCHAR(50) PRIMARY KEY,
          name VARCHAR(50),
          gname VARCHAR(50),
          age INT,
          sex VARCHAR(10),
          address VARCHAR(100),
          date DATE,
          phone VARCHAR(15),
          department VARCHAR(50),
          remark VARCHAR(100)
      );
      ```

3. **Update Database Credentials**:
    - Open `Real.java` and update the database URL, username, and password if necessary:
      ```java
      static final String DB_URL = "jdbc:mysql://localhost:3306/arogya";
      static final String USER = "root";
      static final String PASS = "mysql";
      ```

4. **Compile and Run**:
    - Compile the Java files:
      ```sh
      javac Real.java
      ```
    - Run the application:
      ```sh
      java Real
      ```

## Usage

- **Login**: Use the default credentials `admin` for the username and `admin123` for the password.
- **Patient Registration**: Click on the "Registration" button and fill in the required details.
- **Query System**: Use the "Queries" button to execute specific patient data queries.
- **Export Data**: Click on the "Export" button to export patient data to a CSV file.
- **Display Data**: Use the "Show Data" button to view patient data in the GUI.

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests.

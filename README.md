# Periodic Table Database

This project represents a simple database containing information about chemical elements, including their atomic numbers, symbols, names, atomic masses, melting and boiling points, and types (metal, nonmetal, metalloid). The database can be queried to retrieve detailed information about elements using different types of identifiers, such as atomic number, symbol, or name.

## Project Setup

To set up and run this project, follow these steps:

1. **Clone the Repository**:
   Clone this repository to your local machine using the following command:
git clone https://github.com/dnlmlszl/periodic_table_db

2. **Set Up PostgreSQL Database**:
- Install PostgreSQL if not already installed.
- Create the `periodic_table` database and the necessary tables (elements, properties, and types).
- Import the schema and data into your PostgreSQL instance.

3. **Configure Database Connection**:
Ensure that the correct database credentials (username, password, database name) are configured in the script for accessing the PostgreSQL database.

4. **Running the Scripts**:
- The `element.sh` script accepts an element's atomic number, symbol, or name as an argument and retrieves detailed information about the element from the database.
- The script will return information like the atomic number, symbol, name, atomic mass, melting point, boiling point, and element type (metal, nonmetal, metalloid).

## Usage

### `element.sh` Script

- **Arguments**:
- The script accepts one argument, which can be the atomic number, symbol, or name of an element.

- **Output**:
- If no argument is provided, the script will display a message:  
 `Please provide an element as an argument.`
- If the argument is not found in the database, the script will output:  
 `I could not find that element in the database.`
- If the element is found, the script will display detailed information in the following format:  
 ```
 The element with atomic number <atomic_number> is <name> (<symbol>).
 It's a <type>, with a mass of <atomic_mass> amu.
 <name> has a melting point of <melting_point> celsius and a boiling point of <boiling_point> celsius.
 ```

## File Structure

- `element.sh`: The main script that retrieves information from the database.
- `README.md`: This file, containing project information and setup instructions.
- `periodic_table.sql`: The SQL file containing the schema and sample data for the periodic table database.

## Requirements

- PostgreSQL
- Bash shell
- Basic understanding of SQL queries and bash scripting

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

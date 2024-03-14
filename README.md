# Periodic Table Database

Solution for the [Periodic Table of Elements challenge](https://www.freecodecamp.org/learn/relational-database/build-a-periodic-table-database-project/build-a-periodic-table-database) on [Relational Database](https://www.freecodecamp.org/learn/relational-database/) certification path.

## Test Cases

- **Database Structure Modifications:**
  - Rename the `weight` column to `atomic_mass`.
  - Rename `melting_point` column to `melting_point_celsius` and `boiling_point` column to `boiling_point_celsius`. These columns should not accept null values.
  - Add the `UNIQUE` constraint to the `symbol` and `name` columns from the `elements` table.
  - Ensure `symbol` and `name` columns have the `NOT NULL` constraint.
  - Set the `atomic_number` column from the `properties` table as a foreign key that references the column of the same name in the `elements` table.

- **Types Table:**
  - Create a `types` table that will store the three types of elements. It should have:
    - A `type_id` column that is an integer and the primary key.
    - A `type` column that's a `VARCHAR` and cannot be null. It will store the different types from the `type` column in the `properties` table.
  - Add three rows to your `types` table whose values are the three different types from the `properties` table.
  - Your `properties` table should have a `type_id` foreign key column that references the `type_id` column from the `types` table. It should be an `INT` with the `NOT NULL` constraint.
  - Each row in your `properties` table should have a `type_id` value that links to the correct type from the `types` table.

- **Data Modifications:**
  - Capitalize the first letter of all the `symbol` values in the `elements` table.
  - Remove all the trailing zeros after the decimals from each row of the `atomic_mass` column.
  - Add elements with atomic number 9 (Fluorine) and 10 (Neon) to your database with their respective properties.

- **Git and Scripting:**
  - Create a `periodic_table` folder in the project folder and turn it into a git repository with `git init`.
  - Your repository should have a `main` branch with all your commits.
  - Create an `element.sh` file in your repo folder for the program. Ensure this script file has executable permissions.
  - Running `./element.sh` without arguments should output "Please provide an element as an argument."
  - Running `./element.sh` with an element's atomic number, symbol, or name should output detailed information about the element.
  - If the argument input does not match any element in the database, the output should be "I could not find that element in the database."
  - Commit messages should be appropriately formatted (Initial commit, fix:, feat:, etc.).
  - Delete the non-existent element whose atomic_number is 1000.
  - Your `properties` table should not have a `type` column.
  - Finish your project on the `main` branch with a clean working tree.

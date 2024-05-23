 **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/ecommerce-project.git
   cd ecommerce-project

**Build the project:**
mvn clean install

**Database Setup**
Open MySQL Workbench and connect to your local MySQL server.

Create a new database:
CREATE DATABASE ecommerce_db;

**Run the following SQL script to create necessary tables and insert initial data. You can find this script in the src/main/resources/db directory of the project:**
SOURCE src/main/resources/db/schema.sql;
SOURCE src/main/resources/db/data.sql;


**Update the application properties:
Open src/main/resources/application.properties and update the MySQL connection settings:**

spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect

**Running the Application
Start the Spring Boot application:**

mvn spring-boot:run
Access the application:

Frontend: Open your web browser and navigate to http://localhost:8080
Admin Panel: Navigate to http://localhost:8080/admin (Default admin credentials can be set in the data.sql script)
Contributing
We welcome contributions! Please see CONTRIBUTING.md for more details.

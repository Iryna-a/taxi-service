# taxi-service

Web-application of a simple taxi service where people can register as drivers.

### Functionality

Drivers can:
- Log in/log out.
- View list of their current cars.
- View lists of all drivers, cars and manufacturers.
- Add/delete a driver.
- Add/delete a car.
- Add a driver to a car.
- Add/delete a manufacturer.

### Project structure

The project is built by the N-tire architecture principle. It has 3 layers:
- Presentation (jsp-pages in `webapp/WEB-INF/views` and controllers in `taxi/controllers` for processing HTTP requests).
- Service (classes in `taxi/service` contain all business logic).
- Data access (classes in `taxi/dao` interact with database through CRUD operations).

The project also contains an Authentication filter in `taxi/web.filter` to prevent access to the main functionality for non-logged in users, and a class for connection to the database in `taxi/util`.

The concept of dependency injection implemented through field injection is also used in the code (annotations and injector are in `taxi/lib`).

### Database structure

![diagram](join-db-diagram.png)

### Technologies

- JDK
- Maven 
- JDBC
- JSTL
- JSP
- Tomcat
- MySQL
- HTML
- CSS

### Web-application running

- Clone this project.
- Make sure you have Tomcat 9.0.50 installed.
- Make sure you use MySQL as a database otherwise you need to change a dependency in pom.xml and check SQL syntax in classes in dao package.
- To get the actual parameters of the database tables, run script from the `resources/init_db.sql` file in the Workbench.
- Edit URL, username, password and JDBC driver in `taxi/util/ConnectionUtil.java`.
- Edit Tomcat configuration.
- Run `mvn clean package` in terminal.
- Run the application.

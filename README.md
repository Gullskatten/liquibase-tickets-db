# liquibase-tickets-db
A sample Liquibase setup using [_liquibase-maven-plugin_](https://mvnrepository.com/artifact/org.liquibase/liquibase-maven-plugin) and [_PostgreSQL_](https://www.postgresql.org/).

### Covered in this example:
* A liquibase-hierarchy example.
* How to use _.csv_ files to insert data into tables.
* How to create tables, columns, and set restrictions (constraints).
* How to add/update columns using _changesets_.
* Simple _rollback_ example.
  
### Not covered:
* Extract username/password from the POM (<build>)
* Creating indexes, triggers..

## Installation

#### 1. Open _postgresql_ (ex. through pgAdmin):
* Create a tablespace named 'tickets_db'.
* Create a database named 'tickets'.
(This could be done using a sql-script, but I have not included this in the example).

#### 2. Configure the liquibase-application.

Open the [pom.xml](pom.xml), and change the _configuration_:
* `<url>jdbc:postgresql://localhost/tickets</url>` : If you for some reason created a database with another name, change /tickets to your database name.
* `<username/> / <password/>` : The username / password should not be configured here (in a _real_ project).. :-)

#### 3. Installation
Open a terminal window and run `'mvn clean install'` in the projects root-folder - magic should now happen!

# Golang Stock APIs with Postgres
This is a project with Golang APIs that access and modify a PostgreSQL database. It can create stock data, edit and delete them.


## Technologies Used
* Golang
* PostgreSQL
* Postman

## Dependencies

* Install Go - https://go.dev/doc/install
* Install PostgreSQL - https://www.postgresql.org/download/
* Install Postman - https://www.postman.com/downloads/


## Executing program
* Create stocksdb database in Postgres in terminal 
```
$ psql
username=# CREATE DATABASE stocksdb;
```
* Create table called stocks
```
CREATE TABLE stocks (
  stockid SERIAL PRIMARY KEY,
  name TEXT,
  price INT,
  company TEXT
  );
```
* Download the repository to your computer, go to project file, and run it
```
git clone https://github.com/mobenh/go-postgres
cd go-postgres
go run main.go
```
* Edit .env file with  your database username and password
```
POSTGRES_URL="postgres://username:password@localhost:5432/stocksdb?sslmode=disable"
```
* Test APIs with Postman
  * Create a POST request with localhost:8080/api/newstock
  * Create a GET request with localhost:8080/api/stock
  * Create a GET request with localhost:8080/api/stock/2 (2 being the ID)
  * Create a PUT request with localhost:8080/api/stock/2
  * Create a DELETE request with localhost:8080/api/deletestock/1

# go-lang-mysql-react-crud

## Backend local setup

**Create database 'userdb':**
```
CREATE DATABASE userdb;
```


**Create table 'users':**
```
CREATE TABLE `users` (
  `id` bigint(20) UNSIGNED NOT NULL,
  `first_name` varchar(200) NOT NULL,
  `last_name` varchar(200) NOT NULL,
  `email` varchar(200) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
ALTER TABLE `users`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `id` (`id`);

ALTER TABLE `users`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL 
  AUTO_INCREMENT, AUTO_INCREMENT=11;
```


**Initialize the Go project:**
Initialize the Go project using the following command
```
go mod init backend
```


**Adding the modules required for the project:**
```
go get github.com/gorilla/mux
go get github.com/go-sql-driver/mysql
```
**Run the backend app**
```
go run main.go
```



## Frontend local setup

**Step 1: The npm install installs all modules that are listed on package.json file and their 
            dependencies**
```
npm install
```

**Step 2: Run the Frontend application**
```
npm start
```
Access the URL via browser - http://localhost:3000

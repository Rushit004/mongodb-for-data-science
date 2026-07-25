# 🍃 01 — Basic Commands

Setup notes: throughout this whole `commands/` folder, I'm using database **`office`** and collection **`employees`**, populated from `office-employees.csv`.

---

### 1. Show all databases
```js
show dbs
```
![screenshot](./screenshots/01-1-show-dbs.png)

---

### 2. Create / switch to the `office` database
```js
use office
```
![screenshot](./screenshots/01-2-use-office.png)

---

### 3. Show all collections in the current database
```js
show collections
```
![screenshot](./screenshots/01-3-show-collections.png)

---

### 4. Create the `employees` collection
```js
db.createCollection("employees")
```
![screenshot](./screenshots/01-4-create-collection.png)

---

### 5. Show the current working database
```js
db
```
![screenshot](./screenshots/01-5-current-db.png)

---

### 6. Clear the terminal screen
```js
cls
```
![screenshot](./screenshots/01-6-cls.png)

---

### 7. Drop the `employees` collection 
```js
db.employees.drop()
```
![screenshot](./screenshots/01-7-drop-collection.png)

---

### 8. Drop the `office` database 
```js
db.dropDatabase()
```
![screenshot](./screenshots/01-8-drop-database.png)

---

### 9. Close the shell
```js
exit
```

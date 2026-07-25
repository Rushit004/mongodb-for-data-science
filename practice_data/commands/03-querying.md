# 🍃 03 — Querying Data

`find` is the main method used to query documents: `db.<collection>.find({query}, {projection})`

---

### 1. Display all documents in the collection
```js
db.employees.find()
```
![screenshot](./screenshots/03-1-find-all.png)

---

### 2. Display documents matching a specific value (query parameter)
```js
db.employees.find({ department: "Sales" })
```
![screenshot](./screenshots/03-2-find-query.png)

---

### 3. Display only specific fields (projection parameter)
```js
db.employees.find({}, { _id: false, name: true, salary: true })
```
![screenshot](./screenshots/03-3-find-projection.png)

---

### 4. Sort documents (1 = ascending, -1 = descending)
```js
db.employees.find().sort({ salary: -1 })
```
![screenshot](./screenshots/03-4-find-sort.png)

---

### 5. Limit the number of results returned
```js
db.employees.find().limit(3)
```
![screenshot](./screenshots/03-5-find-limit.png)
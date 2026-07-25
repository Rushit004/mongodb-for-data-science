# 🍃 08 — Indexing

Indexes let MongoDB avoid scanning every document to satisfy a query. Stored as B-Trees; `_id` is indexed by default.

---

### 1. Create an index (ascending, on `department`)
```js
db.employees.createIndex({ department: 1 })
```
![screenshot](./screenshots/08-1-create-index.png)

---

### 2. View all indexes on the collection
```js
db.employees.getIndexes()
```
![screenshot](./screenshots/08-2-get-indexes.png)

---

### 3. Analyze query performance with `explain`
```js
db.employees.find({ department: "Sales" }).explain("executionStats")
```
![screenshot](./screenshots/08-3-explain.png)

---

### 4. Delete an index
```js
db.employees.dropIndex("department_1")
```
![screenshot](./screenshots/08-4-drop-index.png)
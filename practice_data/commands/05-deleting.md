# 🍃 05 — Deleting Data





### 1. `deleteOne` — remove a single document matching a filter
```js
db.employees.deleteOne({ name: "Ryan" })
```
![screenshot](./screenshots/05-1-delete-one.png)

---

### 2. `deleteMany` — remove all documents matching a filter
```js
db.employees.deleteMany({ department: "HR" })
```
![screenshot](./screenshots/05-2-delete-many.png)
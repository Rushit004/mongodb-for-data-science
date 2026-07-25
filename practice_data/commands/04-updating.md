# 🍃 04 — Updating Data

`updateOne` / `updateMany` both take two parameters: `{filter}` and `{update}`.

---

### 1. Change the value of an existing field (`$set`)
```js
db.employees.updateOne(
  { name: "Pamela" },
  { $set: { salary: 55000 } }
)
```
![screenshot](./screenshots/04-1-update-set-existing.png)

---

### 2. Create a new field on a document (`$set`)
```js
db.employees.updateOne(
  { name: "Toby" },
  { $set: { fullTime: true } }
)
```
![screenshot](./screenshots/04-2-update-set-new-field.png)

---

### 3. Remove a field from a document (`$unset`)
```js
db.employees.updateOne(
  { name: "Toby" },
  { $unset: { fullTime: "" } }
)
```
![screenshot](./screenshots/04-3-update-unset.png)

---

### 4. Add a field to every document (`updateMany`, empty filter)
```js
db.employees.updateMany(
  {},
  { $set: { fullTime: true } }
)
```
![screenshot](./screenshots/04-4-update-many-all.png)

---

### 5. Update all documents that match a filter condition
```js
db.employees.updateMany(
  { department: "Sales" },
  { $set: { bonus: true } }
)
```
![screenshot](./screenshots/04-5-update-many-filtered.png)
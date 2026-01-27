# 🦀 Actix-Web CRUD API

Simple **CRUD REST API** built with **Rust** using **Actix-Web** framework.  
Project ini mendemonstrasikan operasi dasar **Create, Read, Update, Delete (CRUD)** menggunakan in-memory storage (`HashMap`) dan cocok untuk **belajar backend Rust / portofolio**.

---

## 📌 Deskripsi

API ini menyediakan endpoint untuk mengelola **Post** yang memiliki:
- `id`
- `title`
- `content`

Data disimpan sementara di memory menggunakan `Mutex<HashMap<usize, Post>>`  
(Tidak menggunakan database).

---

## 📡 Endpoint List

| Method | Endpoint | Deskripsi |
|------|--------|---------|
| GET | `/posts` | Menampilkan semua post |
| GET | `/posts/{id}` | Menampilkan post berdasarkan ID |
| POST | `/posts` | Membuat post baru |
| PUT | `/posts/{id}` | Update post berdasarkan ID |
| DELETE | `/posts/{id}` | Menghapus post berdasarkan ID |

---

## ▶️ Cara Menjalankan Project

### 1️⃣ Clone repository
```bash
git clone https://github.com/Kucing-Dev/CRUD-REST-API.git
cd CrudAPI
```

## 2️⃣ run server
```bash
cargo run
```
server will run on:
```bash
http://127.0.0.1:8080
```

## 🧪 Usage Example (curl)
### ➕ Create Post
```bash
curl -X POST http://127.0.0.1:8080/posts \
-H "Content-Type: application/json" \
-d '{
  "id": 1,
  "title": "Hello",
  "content": "Actix is awesome"
}'
```

Response:
```bash
post created
```

### 📄 Get All Posts
```bash
curl http://127.0.0.1:8080/posts
```

Response:
```bash
[
  {
    "id": 1,
    "title": "Hello",
    "content": "Actix is awesome"
  }
]
```
### 🔍 Get Post by ID
```bash
curl http://127.0.0.1:8080/posts/1
```

### ✏️ Update Post
```bash
curl -X PUT http://127.0.0.1:8080/posts/1 \
-H "Content-Type: application/json" \
-d '{
  "id": 1,
  "title": "Updated",
  "content": "Edited content"
}'
```

Response:
```bash
post updated
```

### 🗑️ Delete Post
```bash
curl -X DELETE http://127.0.0.1:8080/posts/1
```

Response:
```bash
post deleted
```

## ⚠️ Note

- Data is not persistent (lost when the server goes down)
- Suitable for:
    - Learning REST APIs
    - Rust backend practice
    - LinkedIn / GitHub portfolio

## 🚀 Tech Stack

- Rust
- Actix-Web
- Serde
- HashMap + Mutex

## 📌 Author
Khairunnisya Lubis Rust Backend Enthusiast

⭐ If you like this project, feel free to give it a star!

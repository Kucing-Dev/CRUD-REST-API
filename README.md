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
git clone https://github.com/USERNAME/CrudAPI.git
cd CrudAPI

# rust-minigrep

`rust-minigrep` is a simple command-line application (CLI) for searching text within files.  
This project is written in **Rust** and inspired by the *minigrep* example in *The Rust Programming Language* book.

---

## ✨ Features
- Search for a substring in a text file.
- Supports **case-sensitive** search (default).
- Supports **case-insensitive** search by setting the `IGNORE_CASE` environment variable.
- Simple error handling (e.g., when file is missing or arguments are insufficient).
- Includes unit tests to verify search functionality.

---

## 📦 Installation

Clone this repository and navigate to the project folder:

```bash
git clone https://github.com/ParesSensei/rust-minigrep
cd rust-minigrep
```

Build the project:
```bash
cargo build
```

Or run directly:
```bash
cargo run -- <query> <file_path>
```

---

## 📌 Usage

1. Case-sensitive (default)
```bash
cargo run -- duct poem.txt
```
Output:
```bash
safe, fast, productive.
```

2. Case-insensitive
Set the environment variable IGNORE_CASE before running:

Linux / macOS:
```bash
IGNORE_CASE=1 cargo run -- rust poem.txt
```

Windows (PowerShell):
```powershell
$env:IGNORE_CASE=1; cargo run -- rust poem.txt
```

Output:
```angular2html
Rust:
Trust me.
```

---

## 🧪 Testing
Unit tests are included in lib.rs.
To run all tests:
```bash
cargo test
```

---

## 📖 Example Input File (poem.txt)
```txt
Rust:
safe, fast, productive.
Pick three.
Trust me.
```
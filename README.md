# 📝 Automatic Question Paper Generator (PHP + MySQL)

A web-based system that automatically generates question papers from a question bank using predefined patterns and difficulty levels.  
Teachers can create, store, and manage questions, then generate balanced papers in a few clicks.

## 🚀 Features
- ✅ Teacher login & secure admin panel  
- ✅ Question bank with CRUD for questions (MCQ, 2‑mark, 5‑mark, etc.)  
- ✅ Difficulty level & unit/topic-wise tagging  
- ✅ Pattern-based paper generation (marks, sections, number of questions)  
- ✅ Randomization to avoid repetition and leakage  
- ✅ Generated paper preview and print/download option (PDF/HTML)  
- ✅ Course / subject / semester-wise question papers  

## 📂 Project Structure

Automatic-Question-Paper-Generator/

├── index.php              # Landing / login page  
├── home.php               # Dashboard  
├── about.php              # About system  
├── admin/                 # Admin related pages  
├── users/                 # CSS, JS, images  
├── classes/               # Core PHP classes (DB, Question, Paper, User)  
├── database/              # SQL files / migrations  
├── inc/                   # Common includes (header, footer, config)  
├── plugins/               # Third-party libraries (if any)  
├── config.php             # Database configuration  
├── initialize.php         # App bootstrap  
└── README.md  




## 🛠️ Tech Stack
| Component | Technology |
|-----------|------------|
| Frontend | HTML, CSS, Bootstrap, JavaScript |
| Backend  | PHP 8+ |
| Database | MySQL |
| Server   | XAMPP (Apache + MySQL) |
| OS       | Windows |

## 🚀 Quick Setup

1. **Start XAMPP** (Apache + MySQL)

2. **Copy project** to `C:\xampp\htdocs\aqpg`

3. **Create Database**:
```
CREATE DATABASE aqpg;
```

4. **Import schema** from `database/aqpg.sql` via phpMyAdmin

5. **Edit config** (`config.php`):
```
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'aqpg');
```

6. **Open browser**: `http://localhost/aqpg`

**Default Login**: admin / admin123 (change after first login)

## 📊 Sample Database Tables

-- Questions table
CREATE TABLE questions (
id INT AUTO_INCREMENT PRIMARY KEY,
subject VARCHAR(100),
unit_no INT,
question_text TEXT,
type ENUM('mcq','short','long'),
marks INT,
difficulty ENUM('easy','medium','hard'),
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Papers table
CREATE TABLE papers (
id INT AUTO_INCREMENT PRIMARY KEY,
title VARCHAR(200),
total_marks INT,
pattern JSON, -- {"unit1":20, "unit2":25, ...}
generated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


## 📸 Demo Screens

### 🏠 Dashboard
![Dashboard](screenshots/dashboard.png)

### ✏️ Add Question Page
![Add Question](screenshots/add_question.png)

### 📄 Generated Question Paper
![Generated Paper](screenshots/generated_paper.png)

---

👤 Developer  

Built by **NaveenHarshavarthini Ganesan**  

🔗 [LinkedIn](https://www.linkedin.com/in/naveenharshavarthini-ganesan-4047a6311/)  
🔗 [GitHub](https://github.com/Naveenharshavarthini)




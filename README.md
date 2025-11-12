# 📸 veo

A modern platform where creators can upload and manage **stock videos and images**, and subscribers can **preview, search, and download** media assets with ease.  
Built with **FastAPI (backend)** and **Flutter (frontend)** — designed for performance, scalability, and secure media delivery.

---

## 🚀 Project Overview

This project aims to create a high-performance **stock media marketplace** that allows:
- Creators to upload, tag, and manage their photos/videos.
- Users to search media using **hybrid semantic + keyword search**.
- Subscribers to preview and securely download licensed assets.
- Admins to monitor uploads, licensing, and performance analytics.

**Tech Stack**
- 🐍 Backend: [FastAPI](https://fastapi.tiangolo.com/)
- 📱 Frontend: [Flutter](https://flutter.dev/)
- 🔍 Search Layer: Hybrid (Vector + Keyword)
- ☁️ Storage: AWS S3 / GCP Storage (configurable)
- 🗄️ Database: PostgreSQL / Supabase
- 🔒 Auth: JWT-based secure login system

---

## 🧰 Project Structure

stock-media-platform/
│
├── src/ # Backend source (FastAPI app)
│ ├── main.py # Entry point for API server
│ ├── routes/ # API route handlers
│ ├── models/ # Database models (SQLAlchemy)
│ └── services/ # Business logic and integrations
│
├── tests/ # Unit and integration tests
│
├── docs/ # Architecture notes, API docs, design plans
│
├── scripts/ # Utility scripts (e.g., setup, migrations)
│
├── frontend/ # Flutter app (to be linked later)
│
├── .gitignore
├── README.md
└── requirements.txt or pyproject.toml


## ⚙️ Getting Started (Developer Setup)

### 1. Clone the Repository
```bash
git clone git@github.com:pilgrim-AIEngineer/veo.git
cd veo

python -m venv .venv
# Activate on Windows
.venv\Scripts\activate
# Activate on Mac/Linux
source .venv/bin/activate

pip install -r requirements.txt

uvicorn src.main:app --reload

Then open: http://localhost:8000/docs

## 🧪 Testing
```bash
pytest
pytest --cov=src

## 🧭 Milestones Roadmap
### Milestone	Description                                               	Status
0	Environment setup, Git/GitHub init, project structure, README    	✅ Done
1	FastAPI project scaffold, basic health endpoint                 	🔜 Next
2	Database models and hybrid search prototype	                        ⏳
3	Flutter UI skeleton	                                                ⏳
4	Authentication, upload & preview	                                ⏳
5	Subscription system & analytics	                                    ⏳

##🧑‍💻 Contribution Guide

### Fork the repo & create a new branch

git checkout -b feature/your-feature-name


Make your changes and commit using conventional commit messages (e.g., feat: add upload endpoint).

Push to your fork and open a Pull Request to main.

Commit message prefixes

##Type	    Meaning
feat	    New feature
fix	Bug     fix
docs	    Documentation only changes
chore	    Build/maintenance
test	    Testing updates
refactor	Code change that doesn’t alter functionality


## 🧱 Code Style & Tools

Formatter: Black

Linter: Ruff / Flake8

Tests: Pytest

Type Checking: Mypy

CI/CD: GitHub Actions (planned)

###To format and lint:

black .
ruff check .

## 🔐 Environment Variables

Create a .env file in project root:

DATABASE_URL=postgresql://user:pass@localhost:5432/stockmedia
SECRET_KEY=your-secret-key
AWS_ACCESS_KEY=...
AWS_SECRET_KEY=...


(Don’t commit .env — it’s ignored in .gitignore)

## 📜 License

This project is licensed under the MIT License – see the LICENSE
 file for details.

## 🙌 Acknowledgements

Special thanks to the open-source community for the amazing tools powering this project:
FastAPI, Flutter, PostgreSQL, and the contributors that inspire cleaner software every day.
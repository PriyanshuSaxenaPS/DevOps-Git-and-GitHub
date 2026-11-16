# Git & GitHub - DevOps Assignment

This repository contains my completed practical assignment for the **TuteDude DevOps** module. It demonstrates an end-to-end Git and GitHub version control workflow—including SSH setup, parallel feature branching, merge conflict resolution, sequential commits, soft resets, and non-squashed rebasing—built around a full-stack Flask and MongoDB To-Do application.

## 📌 Assignment Objectives
Practise core and advanced Git operations across four structured tasks:
1. **Repository Setup & First Branch**: Configure SSH keys, clone via SSH, commit initial Flask files on a personal branch (`PriyanshuSaxenaPS`), and merge into `main`.
2. **Update JSON & Resolve Conflicts**: Modify `data.json` across branches (`PriyanshuSaxenaPS_new` vs. `main`) and resolve merge conflicts by accepting incoming changes (`--theirs`).
3. **Parallel Feature Development**: Develop a To-Do frontend form on `master_1` and a `/submittodoitem` MongoDB POST route on `master_2`, then merge both into `main`.
4. **Sequential Commits, Reset & Rebase**: Add `Item ID`, `Item UUID`, and `Item Hash` fields in separate commits, roll back `main` using `git reset --soft`, and rebase onto `master_1` while preserving commit history.

---

## 🛠️ Tech Stack & Dependencies
* **Version Control:** Git, GitHub (SSH Authentication)
* **Backend:** Python 3.13, Flask
* **Database:** MongoDB Atlas (`pymongo`, `dnspython`)
* **Environment Management:** `python-dotenv`
* **Frontend:** HTML, CSS (`templates/index.html`, `static/style.css`)

---

## 🚀 Setup & Installation

### 1. Clone the Repository via SSH
```bash
git clone git@github.com:PriyanshuSaxenaPS/Git_and_GitHub.git
cd Git_and_GitHub
```

### 2. Create & Activate a Virtual Environment
```bash
python -m venv venv
# Windows PowerShell:
venv\Scripts\activate
# Linux/macOS:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory and add your MongoDB Atlas URI:
```env
MONGODB_URI="mongodb+srv://<username>:<password>@<cluster-url>/todo_database?retryWrites=true&w=majority"
```

### 5. Run the Flask Application
```bash
python app.py
```
Access the To-Do application locally at `http://127.0.0.1:5000`.

---

## 🌿 Git Workflow Summary

| Branch Name | Purpose |
| :--- | :--- |
| `main` | Primary production branch holding merged features and resolved states. |
| `PriyanshuSaxenaPS` | Initial setup branch for base Flask project files. |
| `PriyanshuSaxenaPS_new` | Used to update `data.json` and demonstrate merge conflict resolution. |
| `master_1` | Frontend To-Do UI development and sequential form field commits. |
| `master_2` | Backend `/submittodoitem` POST endpoint and MongoDB Atlas integration. |

---

## 📂 Repository Structure
* `app.py` — Flask server with `/` and `/submittodoitem` routes and MongoDB connection.
* `data.json` — JSON dataset used for merge conflict testing.
* `requirements.txt` — Python package dependencies.
* `templates/index.html` — Frontend To-Do submission form.
* `static/style.css` — Styling for the To-Do web interface.
* `README.md` — Project overview, setup guide, and branch workflow documentation.

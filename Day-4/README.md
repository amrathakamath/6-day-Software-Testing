
# 🚀 FastAPI Portfolio Deployment & Testing – Day 4 Summary

## 🧩 Session 1: FastAPI Deployment on Render

### ✅ Setting Up the Virtual Environment

```bash
python -m venv ~/profile
source ~/profile/scripts/activate
python -m pip install "fastapi[standard]"
```

### 🛠️ Creating the FastAPI Application

- Navigate to your project directory.
- Create the main application file:
  ```bash
  touch app.py
  code app.py
  ```
- Run the application using Uvicorn:
  ```bash
  uvicorn app:app --reload
  ```
- Create a `templates/` directory and add `index.html` for rendering HTML content.

### 🌐 Deployment on Render

- **Build Command:**
  ```bash
  pip install fastapi "uvicorn[standard]"
  ```

- **Start Command:**
  ```bash
  uvicorn app:app --host 0.0.0.0 --port $PORT
  ```

### 📦 Git Version Control Basics

- Check your changes with:
  ```bash
  git diff
  ```

---

## 🧪 Introduction to Selenium

- Install Selenium:
  ```bash
  python -m pip install selenium
  ```

- Launch a Chrome browser and interact with web elements using:
  ```python
  driver.find_element(...)
  element.send_keys(...)
  ```

---

## 🗂️ Virtual Environment Management

- Created and deleted 10 virtual environments for practice.
- Exited the environment using:
  ```bash
  deactivate
  ```

---

## 🧪 Session 2: Testing and Continuous Integration with GitHub Actions

### 🧩 Adding Automated Tests with FinTest Pro

- Added a `test_main.py` file to test the homepage.
- Used FastAPI's `TestClient` for integration testing.

### ⚙️ Setting Up GitHub Actions for CI/CD

- Created the workflow file: `.github/workflows/main.yml`
- Configured the workflow to:
  - Trigger on push to `main` or any branch
  - Install dependencies
  - Run tests using:
    ```bash
    pytest test_main.py
    ```

### 📄 Adding Dependencies to `requirements.txt`

```
fastapi
uvicorn[standard]
pytest
selenium
```

---

## 📌 Summary

- ✅ Deployed a FastAPI web app on [Render](https://render.com/)
- ✅ Automated testing using `pytest` and `TestClient`
- ✅ Setup CI/CD pipeline with GitHub Actions
- ✅ Practiced web automation using Selenium
- ✅ Managed virtual environments effectively

---
```

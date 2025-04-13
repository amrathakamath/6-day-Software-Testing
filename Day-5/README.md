
# Day 5 Summary

## Session 1: Virtual Environment, Git Workflow, and Selenium

### 1. Virtual Environment
- Discussed the importance of using virtual environments in Python to isolate dependencies.
- Demonstrated how to create and activate a virtual environment:

```bash
python -m venv myenv
myenv\Scripts\activate  # On Windows
```

- Installed required dependencies within the virtual environment.

---

### 2. Git Workflow
- Covered basic Git commands:
  - `git init`
  - `git add`
  - `git commit`
  - `git push`
  - `git pull`
- Demonstrated how to push a project to GitHub and manage repositories.

---

### 3. Selenium Automation with Python
- Installed Selenium and Chrome WebDriver.
- Demonstrated a simple Selenium script:

```python
from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://qxf2.com/selenium-tutorial-main")

name = driver.find_element(by="id", value="name")
name.send_keys("Qxf2")
```

- Explained how to locate elements and perform web interactions using Selenium.

---

## Session 2: API Testing using Postman and Python Requests Library

### 1. Postman API Testing
- Explained the basics of API testing using Postman.
- Demonstrated how to send **GET** and **POST** requests.
- Validated responses using status codes and response body.

---

### 2. API Testing with Python Requests Library
- Demonstrated API testing using Python’s `requests` module.
- Executed a sequence of API calls to a local server (`http://127.0.0.1:5000/`).

#### Sample GET request:
```python
import requests

response = requests.get("http://127.0.0.1:5000/cars", auth=("qxf2", "qxf2"))
print(response.status_code)
print(response.json())
```

#### Sample POST request for adding a new car:
```python
response = my_session.post(url=base_url + 'cars/add', json={
    'name': 'Gwagon',
    'brand': 'Gwagon',
    'price_range': '90-200lacs',
    'car_type': 'sedan'
}, auth=(username, password))
```

- Implemented assertions to validate API responses:

```python
assert response.status_code == 201, f"Expected status 201, got {response.status_code}"
assert 'message' in response_content and 'successfully' in response_content['message'].lower(), "Car addition failed"
```

- Verified that the car count increased after the POST request.

---

## ✅ Conclusion
Today's session covered:
- Setting up and managing virtual environments.
- Basic Git workflow for version control.
- Automating web interactions using Selenium.
- API testing using Postman and Python `requests` library.
- Writing assertions to validate API responses.

This hands-on session helped strengthen practical skills in both **automation** and **API testing**.
```

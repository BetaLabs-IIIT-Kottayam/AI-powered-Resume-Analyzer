# AI Resume Analyzer – Setup Guide

## Requirements

Have these things installed to make your process smooth:

- [Python (3.9.12)](https://www.python.org/downloads/release/python-3912/)
- [MySQL](https://www.mysql.com/downloads/)
- [Visual Studio Code (Preferred Code Editor)](https://code.visualstudio.com/Download)
- [Visual Studio Build Tools for C++](https://aka.ms/vs/17/release/vs_BuildTools.exe)

---

## Setup & Installation

To run this project, perform the following steps:

### 1. Clone the repository

### 2. Create a virtual environment and activate it
```
cd AI-Resume-Analyzer
python -m venv venvapp
cd venvapp/Scripts
activate
```

### Install required packages
```
cd ../..
cd App
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

### 4. Create a database
Create a MySQL database named `"cv"`

###   5. Update database credentials
Edit the file AI-Resume-Analyzer/App/App.py, line 95:

```
connection = pymysql.connect(host='localhost', user='root', password='root@MySQL4admin', db='cv')

```

Go to venvapp\Lib\site-packages\pyresparser folder

And replace the resume_parser.py with resume_parser.py

which was provided by me inside pyresparser folder

### Run the app
Make sure you're in the App directory and your virtual environment is activated:

```
streamlit run App.py
```

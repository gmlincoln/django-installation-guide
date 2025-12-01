# Django Installation Guide

This repository provides step-by-step instructions to install Django and start your first project.

---

## 1. Create a Folder/Directory

```bash
mkdir <folder_name>

#Example:
mkdir "django-intro"

```

## 2. Change Directory

```bash
cd <folder_name>

# Example:
cd django-intro

```
## 3. Create Virtual Environment

```bash

python -m venv <virtual_env_name>
# or on some systems
py -m venv <virtual_env_name>

# Example:
py -m venv myenv

```
## 4. Activate Virtual Environment

```bash

<virtual_env_name>\Scripts\activate   # Windows
# Example:
myenv\Scripts\activate

# or on macOS/Linux
source <virtual_env_name>/bin/activate


```
## 5. Install Django
```bash
pip install django

```
## 6. Verify Installation
Check the installed packages to confirm Django is installed.

```bash
pip list

```

## 7. Create a Django Project

```bash

django-admin startproject <project_name>
# Example:
django-admin startproject myproject

```
## 8. Change Directory to Project

```bash
cd <project_name>

# Example: 
cd myproject

```

## 9. View Project Files

```bash
dir   # Windows
# or
ls    # macOS/Linux

```

## 10. Run Development Server
Start your Django project locally.

```bash
python manage.py runserver

```
Visit http://127.0.0.1:8000/ in your browser to see your project.(locally)

### Project vs App in Django

| **Term**    | **Definition**                                                                                                                   | **Example**                |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| **Project** | The **entire Django website**. It can contain multiple apps. It includes settings, URL configuration, WSGI/ASGI, templates, etc. | `job_portal`               |
| **App**     | A **self-contained module** within a project, focused on **one functionality**. Can be reused in other projects.                 | `accounts`, `jobs`, `blog` |



### MVC vs MVT
Django is technically MVT (Model-View-Template), not MVC, but very similar.

| **Concept**    | **MVC (Classic)**                        | **MVT (Django)**                               |
| -------------- | ---------------------------------------- | ---------------------------------------------- |
| **Model**      | Handles database                         | Handles database                               |
| **View**       | Handles user input & logic               | Handles logic & passes data to Template        |
| **Controller** | Handles interaction between Model & View | Django **framework itself acts as controller** |
| **Template**   | Part of View                             | Handles presentation (HTML)                    |


Django separates logic (View) and presentation (Template) like MVC but the controller is built-in.
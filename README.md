# Workwave-API

Workwave-API is a job portal backend API built with Django and Django REST Framework (DRF), providing functionality for job postings, applications, user account handling, profile management, and job searching. This API powers the backend for Workwave, a platform connecting job seekers with employers.

## Features
- User Authentication (Registration, Login)
- Job Listing and Management
- Job Application Processing
- Profile Management for Job Seekers and Employers
- Job Search Functionality

## Technologies Used
- **Django**
- **Django REST Framework (DRF)**
- **HTML, CSS, JavaScript** for additional static content

---

## API Documentation

Below is a detailed outline of available endpoints across different modules.

---

### 1. **Jobs**

Handles job listings and categories.

| Method | Endpoint                          | Description                                      |
|--------|-------------------------------------|--------------------------------------------------|
| GET    | `/jobs/jobs/`                     | List all job postings                            |
| POST   | `/jobs/jobs/create/`              | Create a new job posting                         |
| GET    | `/jobs/jobs/<int:pk>/`            | Retrieve details of a specific job              |
| GET    | `/jobs/categories/`                | Retrieve all job categories                      |
| GET    | `/jobs/categories/<int:pk>/`       | Retrieve details of a specific job category      |
| GET    | `/jobs/search/`                   | Search for jobs based on criteria                |

---

### 2. **Employers**

User-specific routes for managing employer profiles and job postings.

| Method | Endpoint                                 | Description                                      |
|--------|-------------------------------------------|--------------------------------------------------|
| POST   | `/employers/auth/`                      | Login as an employer                             |
| POST   | `/employers/auth/registration/`         | Register a new employer                          |
| GET    | `/employers/dashboard/`                  | Access the employer's dashboard                  |
| GET    | `/employers/profile/`                    | View employer profile details                    |
| PUT    | `/employers/profile/edit/`               | Update employer profile details                  |
| GET    | `/employers/applications/`               | View applications submitted for jobs by the employer |

---

### 3. **Job Seekers**

Routes for managing job seeker profiles and applications.

| Method | Endpoint                                  | Description                                     |
|--------|--------------------------------------------|-------------------------------------------------|
| POST   | `/job_seekers/auth/`                     | Login as a job seeker                          |
| POST   | `/job_seekers/auth/registration/`        | Register a new job seeker                       |
| GET    | `/job_seekers/dashboard/`                 | Access the job seeker's dashboard               |
| GET    | `/job_seekers/profile/`                   | View job seeker profile details                 |
| PUT    | `/job_seekers/profile/edit/`              | Update job seeker profile details               |
| GET    | `/job_seekers/applications/`              | View all applications submitted by the job seeker |

---

### 4. **Applications**

Routes for managing job applications.

| Method | Endpoint                     | Description                               |
|--------|-------------------------------|-------------------------------------------|
| POST   | `/applications/apply/`       | Create a new job application              |
| GET    | `/applications/<int:pk>/`     | Retrieve details of a specific application |
| PUT    | `/applications/<int:pk>/edit/`| Update an existing application            |
| DELETE | `/applications/<int:pk>/delete/`| Delete a specific application            |

---

## Installation and Setup

To set up the Workwave API on your local machine, follow these commands in sequence:

```bash
# Clone the repository
git clone https://github.com/username/Workwave-API.git

# Navigate to the project directory
cd Workwave-API

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start the development server
python manage.py runserver

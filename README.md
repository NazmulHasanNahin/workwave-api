# Workwave-API

Workwave-API is a backend API for a job portal platform, connecting job seekers and employers. Built with Django and Django REST Framework (DRF), this API provides endpoints for job listings, applications, user profile management, authentication, and job searching.

---

## Table of Contents

1. [Features](#features)
2. [Installation and Setup](#installation-and-setup)
3. [API Documentation](#api-documentation)
4. [Project Structure](#project-structure)

---

## Features

- **Job Listings**: CRUD operations for job postings by employers.
- **Applications**: Job seekers can apply to jobs, and employers can view applications.
- **User Profiles**: Profile management for both job seekers and employers.
- **Authentication**: Registration and login for different user roles.
- **Job Search**: Advanced search to help job seekers find relevant jobs.

---

## Installation and Setup

To set up Workwave-API on your local environment:

```bash
# Clone the repository
git clone https://github.com/username/Workwave-API.git

# Navigate to the project directory
cd Workwave-API

# Install dependencies
pip install -r requirements.txt

# Run migrations to set up the database
python manage.py migrate

# Start the development server
python manage.py runserver


# Applications

- List/Create Applications
  - Endpoint: POST /applications/apply/
  - Description: Create a new job application.

- Application Detail
  - Endpoint: GET /applications/<int:pk>/
  - Description: Retrieve details of a specific application.

- Edit Application
  - Endpoint: PUT /applications/<int:pk>/edit/
  - Description: Update an existing application.

- Delete Application
  - Endpoint: DELETE /applications/<int:pk>/delete/
  - Description: Delete a specific application.

# Employers

- Employer Authentication
  - Endpoints:
    - POST /employers/auth/ – Login
    - POST /employers/auth/registration/ – Registration
  - Description: Register or authenticate as an employer.

- Employer Dashboard
  - Endpoint: GET /employers/dashboard/
  - Description: Access the employer's dashboard.

- Employer Profile Management
  - Endpoints:
    - GET /employers/profile/ – View profile details.
    - PUT /employers/profile/edit/ – Update profile details.

- View Applications for Posted Jobs
  - Endpoint: GET /employers/applications/
  - Description: View applications submitted for jobs posted by the employer.

# Job Seekers

- Job Seeker Authentication
  - Endpoints:
    - POST /job_seekers/auth/ – Login
    - POST /job_seekers/auth/registration/ – Registration
  - Description: Register or authenticate as a job seeker.

- Job Seeker Dashboard
  - Endpoint: GET /job_seekers/dashboard/
  - Description: Access the job seeker's dashboard.

- Job Seeker Profile Management
  - Endpoints:
    - GET /job_seekers/profile/ – View profile details.
    - PUT /job_seekers/profile/edit/ – Update profile details.

- View Submitted Applications
  - Endpoint: GET /job_seekers/applications/
  - Description: View all applications submitted by the job seeker.

# Jobs

- List Jobs
  - Endpoint: GET /jobs/jobs/
  - Description: Retrieve all job postings.

- Job Detail
  - Endpoint: GET /jobs/jobs/<int:pk>
  - Description: Retrieve details of a specific job.

- Create Job Posting
  - Endpoint: POST /jobs/jobs/create/
  - Description: Create a new job posting (employer only).

- Job Search
  - Endpoint: GET /jobs/search/
  - Description: Search for jobs based on criteria.

- List Job Categories
  - Endpoint: GET /jobs/categories/
  - Description: Retrieve all job categories.

- Job Category Detail
  - Endpoint: GET /jobs/categories/<int:pk>/
  - Description: Retrieve details of a specific job category.


Project Structure
Applications: Manages job applications.
Employers: Handles employer-related functionalities, including profile management and job posting.
Job Seekers: Handles job seeker functionalities, including applications and profile management.
Jobs: Manages job listings and job categories.

# EHR InGen

EHR InGen is a Django-based web application designed for generating dynamic graphical user interfaces (GUIs) from .opt files and validating clinical document instances. It leverages the power of Django's templating system, Selenium for web automation, and BeautifulSoup for HTML parsing.

## Table of Contents

- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [Running the Application](#running-the-application)
- [Dependencies](#dependencies)
- [User Flow](#user-flow)
- [Future Enhancements](#future-enhancements)
- [Usage Examples](#usage-examples)

## Features

- **Dynamic GUI Generation**: Convert .opt files into HTML forms.
- **Validation**: Validate clinical document instances in XML format.
- **File Upload**: Upload .opt files and XML/HTML files for processing.
- **MongoDB Integration**: Store and retrieve form data using MongoDB.

## Setup and Installation

### Prerequisites

Ensure you have the following installed:

- Python 3.x
- Django 2.2.3
- MongoDB
- ChromeDriver (for Selenium)
- Google Chrome

### Installation Steps

1. **Clone the Repository**

   ```bash
   git clone <repository-url>
   cd ehr_ingen
   ```

2. **Create a Virtual Environment**

   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure MongoDB**

   Ensure MongoDB is running on your local machine or configure the connection string in the views where MongoDB is accessed.

5. **Set Up Django**

   Apply migrations and create a superuser:

   ```bash
   python manage.py migrate
   python manage.py createsuperuser
   ```

## Running the Application

Start the Django development server:

```bash
python manage.py runserver
```

Access the application at `http://127.0.0.1:8000/`.

## Dependencies

- Django 2.2.3
- Selenium
- BeautifulSoup4
- lxml
- pymongo
- clipboard

Ensure these are listed in your `requirements.txt` file.

## User Flow

1. **Home Page**: Provides options to generate dynamic GUIs or validate documents.
2. **Upload Page**: Allows users to upload .opt files for GUI generation.
3. **Form Page**: Displays the generated form from the uploaded .opt file.
4. **Validation Page**: Allows users to upload XML/HTML files for validation.
5. **Response Pages**: Provide feedback on successful operations.

## Future Enhancements

- **Enhanced Validation**: Improve XML validation with more detailed error reporting.
- **User Authentication**: Implement user roles and permissions for better access control.
- **UI Improvements**: Enhance the user interface for a more intuitive experience.
- **Error Handling**: Add comprehensive error handling and logging.

## Usage Examples

### Uploading an OPT File

1. Navigate to the "Dynamic GUI Generator" section.
2. Select an .opt file and click "Generate form."
3. The application processes the file and redirects to the generated form.

### Validating an XML File

1. Navigate to the "Validator" section.
2. Select an XML file and click "Submit."
3. The application validates the file and displays the result.

---

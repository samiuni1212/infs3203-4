
# Contact List Manager

A Flask-based web application for managing contacts. This application intentionally has some bugs for educational purposes in software testing.

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Git

## Installation Instructions

### Clone the Repository
```bash
git clone <repository-url>
cd lab6
```

### Setting Up Virtual Environment

#### For macOS/Linux:
```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
source venv/bin/activate
```

#### For Windows:
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
venv\Scripts\activate
```

### Install Dependencies

With the virtual environment activated, install the required packages:
```bash
pip install -r requirements.txt
```

## Running the Application

### First Time Setup
When running the application for the first time, the database will be automatically created.

### Starting the Server

#### For macOS/Linux:
```bash
# Make sure your virtual environment is activated
source venv/bin/activate

# Run the application
python3 app.py
```

#### For Windows:
```bash
# Make sure your virtual environment is activated
venv\Scripts\activate

# Run the application
python app.py
```

The application will be available at `http://localhost:5001`

## Application Features

- Create new contacts
- View list of contacts
- Update existing contacts
- Delete contacts
- Search contacts
- RESTful API endpoints

## API Endpoints

- GET `/api/contacts` - List all contacts
- GET `/api/contacts/<id>` - Get a specific contact
- POST `/api/contacts` - Create a new contact
- PUT `/api/contacts/<id>` - Update a contact
- DELETE `/api/contacts/<id>` - Delete a contact

## Project Structure
```
lab6/
├── app.py               # Main Flask application
├── models.py           # Database models
├── forms.py            # Form definitions
├── requirements.txt    # Project dependencies
├── templates/          # HTML templates
│   ├── base.html
│   ├── index.html
│   ├── contacts.html
│   ├── add_contact.html
│   └── update_contact.html
└── static/
    └── js/
        └── search.js
```

## Troubleshooting

### Port Already in Use
If you get an error about port 5001 being in use:
1. Change the port number in `app.py`
2. Or kill the process using the port:
   ```bash
   # For macOS/Linux
   lsof -i :5001
   kill -9 <PID>
   
   # For Windows
   netstat -ano | findstr :5001
   taskkill /PID <PID> /F
   ```

### Virtual Environment Issues
If you have problems with the virtual environment:
1. Delete the `venv` directory
2. Re-create it following the installation steps above

### Database Issues
If you encounter database problems:
1. Delete the `contacts.db` file
2. Restart the application to create a fresh database

## Deactivating Virtual Environment

When you're done working on the project:
```bash
deactivate
```

## Note for Testing

This application contains intentionally introduced bugs for educational purposes in software testing. These bugs are distributed across different components of the application.

# INFS3203-4


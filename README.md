# Simple Flask Web Application
This is a simple Flask web application that allows users to manage a list of items. Users can view all items, add new items, and delete existing items. The application uses SQLite for data storage and SQLAlchemy as the ORM.

## Project Structure
flask_app/
│
├── app.py
├── models.py
├── templates/
│   ├── base.html
│   ├── index.html
│   └── add_item.html
└── requirements.txt


## Pages and Their Functionalities

1. **Home Page (`/`)**
   - **Route**: `/`
   - **Template**: `index.html`
   - **Functionality**: Displays a list of all items in the database. Each item has a delete link to remove it from the list.

2. **Add Item Page (`/add`)**
   - **Route**: `/add`
   - **Template**: `add_item.html`
   - **Functionality**: Provides a form to add a new item. When the form is submitted, the new item is added to the database, and the user is redirected to the home page.

3. **Delete Item (`/delete/<int:id>`)**
   - **Route**: `/delete/<int:id>`
   - **Functionality**: Deletes the item with the specified ID from the database and redirects the user to the home page.

## Templates

1. **Base Template (`base.html`)**
   - Provides a common structure for all pages.

2. **Home Page Template (`index.html`)**
   - Displays the list of items and provides links to delete items and add new items.

3. **Add Item Page Template (`add_item.html`)**
   - Provides a form to add a new item.

## Requirements

- **File**: `requirements.txt`
- **Purpose**: Lists the dependencies required to run the application.
- **Dependencies**:
Flask==2.0.1 Flask-SQLAlchemy==2.5.1


## Running the Application

1. **Install Dependencies**:
 ```sh
 pip install -r requirements.txt
 python app.py
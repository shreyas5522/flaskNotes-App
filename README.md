
# Simple Flask Notes App

This is a simple Flask application for managing notes. Users can register, log in, create, and view their notes.

## Getting Started

Follow these instructions to set up and run the application on your local machine.

### Prerequisites

- Python (3.6 or higher)
- MySQL server

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-flask-notes-app.git
   ```

2. Change into the project directory:

   ```bash
   cd your-flask-notes-app
   ```

3. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   ```

4. Activate the virtual environment:

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS and Linux:

     ```bash
     source venv/bin/activate
     ```

5. Install the required packages:

   ```bash
    pip install Flask Flask-SQLAlchemy Flask-Login Flask-Bcrypt
   ```

### Configuration

1. Set up your MySQL database and configure the connection in `app.py`:

   ```python
   app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://your-username:your-password@localhost/sflask'
   ```

   Update `your-username` and `your-password` with your MySQL credentials.

2. Create the necessary tables in your MySQL database:

   ```bash
   python
   from app import db
   with app.app_context():
       db.create_all()
   ```

### Running the Application

1. Run the Flask application:

   ```bash
   python app.py
   ```

2. Open your web browser and navigate to [http://127.0.0.1:5000/](http://127.0.0.1:5000/) to access the app.

## Usage

- Register a new account.
- Log in with your credentials.
- Create, view, and manage your notes.

## Contributing

Feel free to contribute to this project by opening issues or submitting pull requests.

## License

This project is licensed under the MIT License
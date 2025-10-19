# airbnb-clone-project
AirBnB Server-Side Logic Clone


🏠 AirBnB Clone - The Console
📄 Project Overview
The AirBnB Clone project is the foundation of a full web application that mimics the functionality of the real Airbnb platform.
 It’s designed to teach and demonstrate full-stack web development principles — starting from backend logic to frontend integration.
In this project, we begin by building a command-line interpreter (console) to manage the application's data models.
 This includes creating, retrieving, updating, and deleting data (objects) related to users, places, cities, and more.
 Later stages of the project will expand this base into a RESTful API, a dynamic web interface, and finally a complete deployment-ready system.
The AirBnB Clone demonstrates essential backend skills such as object-oriented programming (OOP), serialization/deserialization, file storage, database integration, and API development.

🎯 Description of the Command Interpreter
The command interpreter (or console) is the starting point of the project.
 It serves as a backend management tool for manipulating data without using a visual interface.
It allows users to:
Create new objects (e.g., User, Place, City, Review)


Retrieve objects from storage


Perform updates on existing objects


Delete objects when no longer needed


Persist data between sessions using file storage (JSON)


The console acts as the bridge between the developer and the application’s backend — similar to how Django or Flask shells interact with databases.
🔧 How It Works:
The console is built using Python’s cmd module`, which enables the creation of command-line programs.


Data persistence is achieved through a JSON-based storage engine (FileStorage).


Each model (User, State, Place, etc.) inherits from a common BaseModel, which manages unique IDs and timestamps.


Example usage:
(hbnb) create User
(hbnb) show User 1234-5678-9101
(hbnb) update User 1234-5678-9101 email "zee@alxafrica.com"
(hbnb) destroy User 1234-5678-9101


🧱 Command Interpreter Usage
🔹 How to Start It
Run the executable Python file:
$ ./console.py

🔹 How to Use It (Interactive Mode)
$ ./console.py
(hbnb) help
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update
(hbnb)
(hbnb) quit
$

🔹 How to Use It (Non-Interactive Mode)
You can also run commands directly:
$ echo "create User" | ./console.py
$ echo "show User 1234-5678" | ./console.py


🧩 Environment Setup
Requirements:
Ubuntu 20.04 LTS


Python 3.8.5


pycodestyle for linting


Git for version control


Installation:
$ git clone https://github.com/<your-github-username>/AirBnB_clone.git
$ cd AirBnB_clone
$ ./console.py


🧠 Project Structure
AirBnB_clone/
│
├── models/
│   ├── base_model.py
│   ├── user.py
│   ├── state.py
│   ├── city.py
│   ├── place.py
│   ├── amenity.py
│   ├── review.py
│   └── __init__.py
│
├── tests/
│   ├── test_models/
│   │   └── test_base_model.py
│   └── test_console.py
│
├── console.py
├── models/engine/
│   ├── file_storage.py
│   └── __init__.py
│
├── README.md
└── AUTHORS


🧰 Classes and Methods
Class
Description
BaseModel
Defines common attributes/methods for all models
User
Handles user information (email, password, etc.)
State
Defines states within the system
City
Defines cities associated with states
Place
Represents accommodation listings
Review
Stores user feedback about a place
Amenity
Lists features of a place (WiFi, pool, etc.)


⚙️ Storage Engine
🔸 FileStorage
The FileStorage engine serializes instances to a JSON file (file.json) and deserializes JSON back into object instances.
 It serves as the project’s database in early stages.
Functions include:
all() → returns a dictionary of all stored objects


new(obj) → adds a new object


save() → writes objects to file


reload() → loads objects from file


Later stages of the project may introduce DBStorage (SQL-based).

🧪 Testing
Unit tests ensure that every class, method, and feature works as intended.
 Tests are written using Python’s built-in unittest module.
To run all tests:
$ python3 -m unittest discover tests


🧱 Technologies Used
Technology
Purpose
Python 3.8.5
Core language used
cmd module
Console command framework
JSON
File-based data storage
unittest
Automated testing
Git & GitHub
Version control and collaboration
pycodestyle (PEP8)
Code formatting standard


🌍 Deployment
While the console is locally run, future phases of the project will involve:
Creating REST APIs with Flask


Storing data in MySQL/PostgreSQL


Deploying with Gunicorn, Nginx, or Render


Integrating the backend with a responsive HTML/CSS/JS frontend



👨‍💻 Authors
This project was completed as part of the ALX Software Engineering Programme.
Contributors:
Zee [zeecaptcha]



🏁 License
This project is part of the ALX curriculum and is distributed under the MIT License.
 See the LICENSE file for details.

💬 Acknowledgments
Special thanks to the ALX Africa team, mentors, and peers for providing guidance, code reviews, and support throughout the project.


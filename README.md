
# 🎬 Movie Listing API

A production-ready RESTful API for managing movies, user interactions, and community engagement, built with FastAPI.

This system enables users to register, authenticate, and interact with movie content through ratings, comments, and nested discussions, simulating real-world media platforms.

## 🚀 Features

### -User Authentication
    - Register new users
    - Login with email & password

### Movie Management
    - List all movies
    - Retrieve a movie by ID
    -Create, update, delete movies

### Comments
    - Add comments to movies
    - Retrieve comments for a movie
    - Add nested replies to comments

### Ratings
    - Rate movies
    - Retrieve average rating for a movie

## 📦 Getting Started

### Prerequisites
Make sure you have the following installed:
    - Python 3.9+
    -pip (Python package manager) 


### 🛠 Installation Steps

1. **Clone the repository:**

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Create a virtaul enviroment and install the dependecies**

    ```sh
    python3 -m venv venv
    ```

     ```sh
    pip3 install -r requirements.txt
    ```

3. **Run the application: Go a step back from the root directory and run:**

    ```
   uvicorn app:main.app --reload
    ```

4. **The application will be available at:**

    ```
    http://localhost:8000 
    ```
5. **The swagger documentation will be available at:**

    ```
    http://localhost:8000/docs
    ```

## API Endpoints

The API includes the following endpoints (available in the Swagger docs):

### 🔐 User

- ** POST** ``/signup`` - Create a new user account
- ** POST** ``/signup`` - Create a new user account

###  🎥 Movies

- GET ``//movies/`` - List all movies
- GET ``//movies/{movie_id}`` - Get movie by ID
- POST ``/movies/create`` – Create a new movie
- PUT ``/movies/{movie_id}`` – Update existing movie
- DELETE ``/movies/{movie_id}`` – Delete a movie

### 🗨️ Comments

- POST ``/movies/{movie_id}/create_comment`` – Add a comment
- GET ``/movies/{movie_id}/comments`` – List movie comments
- POST ``/comments/{comment_id}/comments`` – Add nested comment

## ⭐ Ratings
- POST ``/movie/{movie_id}/create_rating`` – Create a rating
- GET ``/movie/rating/{movie_id}`` – Get movie rating


### Environment Variables

"db_url" = Database Url
ALGORITHM = Algorthing for creating access token
SECRET_KEY = Secret Key for creating access token

Create a `.env` file in the root directory and add your environment variables:

## Testing


### Steps

1. **CD into the root directory**
    ```
    cd capstone_main
    ```


1. **Run pytest on your terminal**
    ```
    pytest
    
    ```

### 📌 Technologies Used

- FastAPI – Backend framework
- Uvicorn – Asynchronous server
- SQLAlchemy – ORM for database interactions
- Alembic – Database migrations
- Pytest – Testing

### Demo Link

Visit the [DEMO LINK](https://capstone-main.onrender.com/docs)

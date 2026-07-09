# 🎬 Movie Listing API

A production-ready RESTful API for managing movies, user interactions, and community engagement — built with **FastAPI**. Users can register, authenticate, and interact with movie content through ratings, comments, and nested discussion threads, simulating a real-world media platform.

**🔗 Live demo:** [capstone-main.onrender.com/docs](https://capstone-main.onrender.com/docs)

---

## 🚀 Features

**User Authentication**
- Register new users
- Login with email & password
- JWT-based access token authentication

**Movie Management**
- List all movies
- Retrieve a movie by ID
- Create, update, and delete movies

**Comments**
- Add comments to movies
- Retrieve all comments for a movie
- Add nested replies to comments (threaded discussions)

**Ratings**
- Rate movies
- Retrieve average rating for a movie

---

## 📦 Getting Started

### Prerequisites
- Python 3.9+
- pip (Python package manager)

### 🛠 Installation

**1. Clone the repository**
```sh
git clone <repository-url>
cd <repository-directory>
```

**2. Create a virtual environment and install dependencies**
```sh
python3 -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip3 install -r requirements.txt
```

**3. Set up environment variables**

Create a `.env` file in the root directory:
```env
DB_URL=your_database_url
SECRET_KEY=your_secret_key_for_signing_tokens
ALGORITHM=HS256
```

**4. Run the application**
```sh
uvicorn app.main:app --reload
```

**5. Access the app**
- API base: `http://localhost:8000`
- Swagger docs: `http://localhost:8000/docs`

---

## 📖 API Endpoints

Full interactive docs available via Swagger at `/docs`. Summary below:

### 🔐 User
| Method | Endpoint | Description |
|---|---|---|
| POST | `/signup` | Create a new user account |
| POST | `/login` | Authenticate and receive access token |

### 🎥 Movies
| Method | Endpoint | Description |
|---|---|---|
| GET | `/movies/` | List all movies |
| GET | `/movies/{movie_id}` | Get movie by ID |
| POST | `/movies/create` | Create a new movie |
| PUT | `/movies/{movie_id}` | Update an existing movie |
| DELETE | `/movies/{movie_id}` | Delete a movie |

### 🗨️ Comments
| Method | Endpoint | Description |
|---|---|---|
| POST | `/movies/{movie_id}/create_comment` | Add a comment |
| GET | `/movies/{movie_id}/comments` | List comments for a movie |
| POST | `/comments/{comment_id}/comments` | Add a nested reply |

### ⭐ Ratings
| Method | Endpoint | Description |
|---|---|---|
| POST | `/movie/{movie_id}/create_rating` | Submit a rating |
| GET | `/movie/rating/{movie_id}` | Get average rating for a movie |

---

## 🧪 Testing

```sh
cd capstone_main
pytest
```

---

## 📌 Technologies Used

- **FastAPI** – Backend framework
- **Uvicorn** – ASGI server
- **SQLAlchemy** – ORM for database interactions
- **Alembic** – Database migrations
- **JWT** – Authentication
- **Pytest** – Testing

---

## 👤 Author

**Sixtus Omeje**
Backend Developer — Python / FastAPI
[LinkedIn](https://www.linkedin.com/62s) · [GitHub](https://github.com/SixtusNnanna)

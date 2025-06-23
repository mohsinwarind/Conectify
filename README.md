
# 🌐 Conectify

**Conectify** is a Django-based social media platform that allows users to create, share, and interact with posts. It supports user authentication, profile customization, image uploads, follow systems, and more.

---

## 🚀 Features

* ✅ **User Registration & Authentication**

  * Sign up and log in securely
  * Session-based authentication
* 🌍 **Public Post Browsing**

  * View all posts even without logging in
* 📝 **Create a Post**

  * Add text content
  * Attach an image from your local storage or via URL
* ❤️ **Engagement**

  * Like & comment on posts (available to logged-in users)
* 🔄 **Follow System**

  * Follow or unfollow other users
  * View posts only from users you follow
* 👤 **User Profiles**

  * Upload or update profile pictures
  * View your followers and following count
  * Visit other users' profiles and view their posts
* ⚙️ **Profile Management**

  * Edit your profile details and image

---

## 🛠️ Tech Stack

| Component      | Technology           |
| -------------- | -------------------- |
| Backend        | Django               |
| Frontend       | HTML, CSS, Bootstrap |
| Database       | SQLite (default)     |
| Image Handling | Pillow               |
| Authentication | Django Auth System   |

---

## 📂 Project Structure

```
conectify/
├── manage.py
├── conectify/            # Project settings
│   └── settings.py
├── network/              # Main app
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── templates/
│   │   ├── layout.html
│   │   ├── index.html
│   │   └── ...
│   └── static/
│       └── ...
```

---

## 🧪 Core Functionalities

### 🧑‍💻 User System

* `/register`: Sign up for a new account
* `/login`: Log in to your account
* `/logout`: Log out from the platform

### 📸 Post Management

* `/create`: Create a new post with optional image
* Supports both:

  * Local file upload
  * External image URL

### 💬 Interactions

* Like/Unlike posts
* Comment on posts
* See number of likes and comments

### 🔁 Follow Feed

* Homepage feed shows posts from followed users
* See "Follow" and "Unfollow" buttons on user profiles

### 📇 User Profile

* `/profile/<username>`: View user profile
* Display:

  * Profile picture
  * Post count
  * Follower/Following counts
  * Their posts

---

## 📷 Image Uploads

Supports:

* Local file uploads using `<input type="file">`
* External image URLs via a form field

Stored in:

* `media/` directory (ensure MEDIA settings are configured)

---

## ⚙️ Configuration

### `settings.py`

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

### `urls.py`

```python
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    # ... your routes
] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

---

## 🧑‍🏫 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/conectify.git
cd conectify
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Migrations

```bash
python manage.py migrate
```

### 5. Run the Development Server

```bash
python manage.py runserver
```

### 6. Access the App

Open in your browser: `http://127.0.0.1:8000/`


---

## 📌 To-Do / Future Features

* [ ] Notifications for new followers or likes
* [ ] Direct messaging
* [ ] Hashtag support
* [ ] Infinite scroll / Pagination
* [ ] API (Django REST Framework)
* [ ] Unit Tests

---

## 🤝 Contributing

Contributions, suggestions, or issue reports are welcome! Feel free to fork and submit a PR.

---

## 📜 License

This project is licensed under the MIT License.

---

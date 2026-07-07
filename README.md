# Birthday Manager (ACME Project)

A web application built with **Django 6.x** that allows users to register, log in, and manage a database of birthdays. The project is designed with robust security standards, proper git configurations, and is ready for further feature expansions.

---

## 🚀 Features

### Currently Implemented
* **User Authentication & Management**: 
  * Full registration and secure login system.
  * Secure logout workflow utilizing **POST requests** compliant with Django 6.x security updates.
  * Account deletion feature for user privacy.
  * Embedded workflows for password changes and resets.
* **Birthday Database**: Stores and tracks user-submitted birthdays.
* **Clean Architecture**: Uses Django's built-in auth apps linked under the `/auth/` routing prefix.
* **Repository Protection**: Pre-configured `.gitignore` preventing local sqlite databases, virtual environments, and media directories from leaking into production.

### Future Roadmap
* 📅 **Reminders & Alerts**: Automated email notifications before upcoming birthdays.
* 👥 **Social Sharing**: Ability to share birthday wishlists or countdowns with friends.
* 📊 **Analytics Dashboard**: Visual charts showing upcoming celebrations by month or zodiac signs.

---

## 🛠️ Getting Started

Follow these steps to set up and run the project locally on your machine.

### Prerequisites
Make sure you have Python 3.10+ installed. You can check your version by running:
```bash
python --version
```

### Installation

1. **Clone the repository:**
   ```bash
   git clone
   
   cd your-repo-name
   ```

2. **Create and activate a virtual environment:**
   * On Windows:
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```
   * On macOS/Linux:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install dependencies:**
   *(Ensure you have Django installed or run the following command if you have a requirements.txt file)*
   ```bash
   pip install django
   ```

4. **Apply database migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for admin panel access):**
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server:**
   ```bash
   python manage.py runserver
   ```

Now open your browser and navigate to `http://127.0.0`. To log in, use the secure endpoint at `http://127.0.0auth/login/`.

---

## 📂 Project Structure Highlights
* `acme_project/urls.py` - Core routing, separating main pages, birthdays, and authentication.
* `templates/registration/` - Contains customization templates like `login.html`.

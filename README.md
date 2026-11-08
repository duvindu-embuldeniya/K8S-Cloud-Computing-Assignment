# K8S-Microservices-Deployment

Django app, split into two services:

- `services/user_service` -> auth, registration, profile management
- `services/chatroom_service` -> rooms, messages, topics, activity feed

## Setup

### 1. Clone the repo and enter the project folder

```bash
git clone <repo-url>
cd K8S-Microservices-Deployment
```

### 2. Create and activate a virtual environment

Windows (PowerShell):
```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```

macOS/Linux:
```bash
python -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up the `.env` file

Copy `env.sample` to `.env` in this folder. It lists several keys (AWS, email, etc.) but those are for optional/unused features right now - for running locally you only need to fill in:

```
SECRET_KEY=
```

Leave the rest blank. Ask **Duvindu** (project owner) for the `SECRET_KEY` to use locally.

### 5. Run migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Start the dev server

```bash
python manage.py runserver
```

App will be available at http://localhost:8000/

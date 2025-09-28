#Week 5 Assignment

# Django Hello World (JSON)

Small Django app with one route that returns the exact JSON:

{"Message": "Hello World!"}

Requirements
Python 3.10+ (3.11+ recommended)

pip + venv

Git

Quick Start
1) Clone and set up
git clone https://github.com/Sanath10591/SoftwareArchitecture.git
cd https://github.com/Sanath10591/SoftwareArchitecture.git

python -m venv .venv
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt

2) Run the app
   
python manage.py runserver
The server starts at: http://127.0.0.1:8000/

3) Hit the endpoint
Open in a browser:

http://127.0.0.1:8000/hello/
You should see:

{"Message": "Hello World!"}
Or via curl:

curl http://127.0.0.1:8000/hello/

Project structure

.
├─ manage.py
├─ requirements.txt
├─ helloworld/
│  ├─ settings.py
│  └─ urls.py
└─ api/
   ├─ views.py
   └─ urls.py
Notes
No database setup needed.

If packages change, update with pip freeze > requirements.txt.

To stop the server: CTRL+C.

If you get import/URL errors, verify:

api is in INSTALLED_APPS (in helloworld/settings.py)

helloworld/urls.py includes path('', include('api.urls'))

api/urls.py defines urlpatterns = [path('hello/', views.hello)]

Tested with
Django 5.x

Python 3.11

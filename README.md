# quiz_api

Steps to run the application

Virtual Environment : Create virtual environment using command virtualenv python_test_env

Activate Environment : Activate the virtual environment using command source python_test_env/bin/activate

Requirements : Install the requirements in virtual environment using command pip install -r docs/requirements.txt

Make Migrations : python manage.py makemigrations

Migrate : Create database using command python manage.py migrate

Load Dummy Data : Load dummy data using command python manage.py initdata

Run the Server : Start the server using command python manage.py runserver

Demo accounts

    username - admin1, password - neosofttech

    username - aayush, password - neosofttech

    username - firoj, password - neosofttech

    username - mohit, password - mohit123

    tanant - neosoft api-key - 23cb00a63d7945eba0ff5b846de1b728

    tenant - webwerks api-key - 3c1a5d88ac914da6a92e860789453779

apis

    Get access token
        url - /api-token-auth/
        method - POST
        params - username, password - Pass these parameters in body eg. {"username" : "user1", "password" : "password1"}

    Get questions
        url - /questions
        method - GET
        headers - token, api-key - pass these parameters in heade section
        params - q (optional)


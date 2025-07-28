# Lab: Authenticating Users
This lab sets up a basic login feature using flask-restful building on the previous lab of a blog site 

## Getting Started
* Set up your virtual enviroment
  ```bash
  virutalenv venv
  source venv/bin/activate
  ```
* Install necessary dependencies
  ```bash
  pip install flask-sqlalchemy flask-migrate
  pip install flask-RESTful
  pip install marshmallow
  pip install faker
  npm install --prefix client
  ```
* Upgrade and seed the database if necessary
  ```bash
  cd server
  flask db upgrade
  python seed.py
  ```

## Running the Application
Run the flask server: <br>
```bash
python app.py
```
Run React in another terminal:
```bash
npm start --prefix client
```

## API Endpoints
* `/login` <br>
post request that gets a username from request.get_json() and set's the session's user_id value to the user's id and returns the user
* `/logout` <br>
Removes the user_id value from the session and returns a 204 status code
* `/check_session` <br>
Retrieves the user_id value from the session. If the session has a user_id, returns the user as JSON with a 200 status code, otherwise returns no data and a 401 status code <br>
**Example Response:**
  ```JSON
  {
      "articles": [],
      "id": 10,
      "username": "Jesse"
  }
  ```

## Front End Visual
![alt text](<Screenshot 2025-07-28 at 1.20.50 PM.png>)
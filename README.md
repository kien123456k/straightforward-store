# 🏪 Straightforward Store API

## Description
This is API for stores management with 3 entities `Store`, `Item` and `User`.

This application authenticates with JWT as an access token as well as a refresh token and blocklist.

## Technology
- Backend
  - Flask - Server Core
  - Postgres + Heroku - Database Server
  - Flask-JWT-Extended - Authentication
  - Flask-RESTful - APIs Builder
  - Flask-SQLAlchemy - Object Relational Mapping
  - uwsgi + psycopg2 - Production
- Tool
  - Postman - Platform for building and using APIs
  - Heroku - Platform as a service

**Note**: I don't intend to create Frontend for this API. But maybe I will in the future. 
##  Document
Import `postman_collection.json` and `postman_environment` into Postman to see API clearly. 

All APIs start with prefix "/api". Below is list of all APIs:


|     endpoint     |  method  |     endpoint     |  method  |
|:----------------:|:--------:|:----------------:|:--------:|
|  /login          |   post   |  /register       |   post   |
|  /refresh        |   post   |  /logout         |   post   |
|  /stores         |   get    |  /store/:name    |  delete  |
|  /store/:name    |   post   |  /store/:name    |   get    |
|  /items          |   get    |  /item/:name     |   get    |
|  /item/:name     |   post   |  /item/:name     |  delete  |
|  /item/:name     |   put    |
|  /user/:id       |  delete  |  /user/:id       |   get    |


## Project setup
### ⚙️ For local environment (SQLite)
- Using virtualenv library to create virtual environment for this project.
- Install dependencies:
```
pip install -r requirements.local.txt
```
- Bootstrap project:
```
python app.py
```

### ⚙️ For production (Heroku + Postgres)
- Procfile tells Heroku what to do
- uwsgi.ini contains information to bootstrap application
- runtime.txt and requirements.txt include all required dependencies and environment

# License & copyright

© Kirin Tran, FPT University TP.HCM
Licensed under the [MIT LICENSE](LICENSE).
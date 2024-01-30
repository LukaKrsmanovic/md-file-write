# Immobilium Project Setup

 Clone the repository and checkout to branch IMMOBILIUM branch.
 ```
 git checkout immobilium
 ```
 
## Postgres and pgAdmin 4 setup

1. Install postgresql-14 on your machine
 
2. Install **pgAdmin 4** for database setup and then:
    - open the app and create server `immobilium-server`
    - switch to connection tab and set following values:
      - Host name/address: localhost
      - Port: 5432
      - Maintenance database: postgres
      - Username: postgres
      - Password: 123456 
> **Note:** Password must be the same as the one for **postgres** user. 


## Database

After installing postgres:
1. Create database `immobilium`
2. Install postgis and hstore:
    - right click on your database, click **Query tool**
    - run `CREATE EXTENSION hstore;`
    - run `CREATE EXTENSION postgis;`

## Setup Project Enviroments

1. Go to frontend folder and create **.env** file from **.env.example**
    ```
    cp .env.example .env
    ```
2. Go to server folder and create **.env** file from **.env.example**
    ```
    cp .env.example .env
    ```

## Install Project

1. Go to frontend folder
    ```
    npm install
    ```
2. Go to server folder
    ```
    npm install
    ```

## Run Project

1. Start Server
    ```
    npm run start:server
    ```
2. Start Frontend
    ```
    npm run start:frontend
    ```



## Frontend .env variables

Some of the frontend enviroment variables explained:

| VARIABLE                   	  | DESCRIPTION                                                  	  	    |
|---------------------------------|---------------------------------------------------------------------------------|
| PORT                       	  | local port for frontend 'localhost:3065'                              	    |
| NODE_ENV                   	  | environment variable in React used to specify the current environment 	    |
| REACT_APP_API_URL          	  | immobilium server (backend) url                             	  	    |
| REACT_APP_GOOGLE_API_KEY   	  | api key for google (maps)                                    	  	    |
| REACT_APP_MAP_LAT          	  | env variable for default map latitude                         	  	    |
| REACT_APP_MAP_LNG          	  | env variable for default map longitude                        	  	    |
| REACT_APP_MAP_ZOOM         	  | env variable for default map zoom                             	  	    |
| REACT_APP_REFRESH_COIN_INTERVAL | represents the time interval (in milliseconds) for refreshing coin-related data |


## Server .env variables

Some of the server enviroment variables explained:

| VARIABLE                | DESCRIPTION                                              		  |
|-------------------------|-----------------------------------------------------------------------|
| PORT                    | local port for frontend 'localhost:5565'                		  |
| NODE_ENV                | variable in React used to specify the current environment 		  |
| WEBSITE_URL             | frontend URL                                             		  |
| SERVER_URL              | server (backend) URL                                    		  |
| DB_...                  | database setup variables (e.g. DB_NAME)                		  |
| JWT_SECRET              | defines a secret key for JSON Web Token                  		  |
| JWT_EXPIRY_TIME         | user authenticated time in milliseconds                 		  |
| UPLOAD_DIR              | default image upload directory                           		  |
| DATA_LIMIT              | when the database is empty, 10 properties will be added  		  |
| MAILGUN_...             | MAILGUN setup variables                                 		  |
| COINMARKETCAP_...       | COINMARKETCAP setup variables                            		  |
| OPENEXCHANGERATES_...   | OPENEXCHANGERATES setup variables                        		  |
| BASE_CURRENCY           | base currency for property prices                        		  |
| ONDATO_KYC...           | ONDATO_KYC setup variables                               		  |
| UTRUST_...              | UTRUST setup variables                                   		  |
| NODE_ADDRESS            | the web interface to the zbs full node API                		  |
| SERVER_SEED             | seed words for the wallet                                 		  |

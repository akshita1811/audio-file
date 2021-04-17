# filed_audio_file_server

This is Test challenge by filed


##setup the system

1. Setup codebase
 
    1. clone the code in a directory
      
            git clone https://github.com/sahasrara62/filed_audio_file_server.git
    2. go in the directory `cd filed_audio_file_server`
    3. install all project requirements, use command
        `python -m pipenv install -r requirements.txt`
    4. go in `pipenv` virtualenv by `python -m pipenv shell`
    5. set up flask env variable, run commands
        1. `export FLASK_APP=main.py`
        2. `export FLASK_ENV=developement`

2. create database
        
      in postgresql create database "audioserver" and grant permission to user, in postgresql shell run command .
      
       1. create db audioserver;
       2. GRANT ALL PRIVILEGES ON DATABASE audioserver to "prashant"; # my username

3. create the table in audioserver database
     1. in `.env` file add the data as below
            
            # example
            # DATABASE_URL="postgresql://prashant:rana@localhost:5432/audioserver"
            DATABASE_URL="postgresql://<username>:<password>@<server host>:<port>/<database name>
            SECRET_KEY="this-is-a-sample-secret-key"
            FLASK_ENV="development"
            SQLALCHEMY_TRACK_MODIFICATIONS=True
     2. lets do migrations, run following commands
        1. `flask db init`
        2. `flask db migrate`
        3. `flask db upgrade`
       
        this  will create a migration folder, and create table in the database
4. run app, activate envrionment `pipenv shell` and run the command to run server
    `flask run`
5. check if server is running, in browser go to `localhost:5000/`, you will get `server is running` msg.

            
     



# DockerKit for Python
It will provide you with a rapid development and testing environment for Python. This package is included **Python**, **PostgreSQL**, **Redis**, **Nginx** tools. 

## How can use?
First of all, run ```pip3 freeze > requirements.txt``` in the directory where your Python project is and replace the resulting **requirements.txt** file with the empty file in the main directory of this project. (This is required to install dependencies.)

Then you should add a shortcut named **code** in this directory from the directory where your python codes are located. (For example: ```ln -s ~/Desktop/yourPythonAppLocation code```)

**IMPORTANT** Please check **docker-compose.yml** file for your project and Python command.

Let's do this, it's ready for starting! ```docker-compose up```

Now we can access services.
```
NGINX Web Server: http://localhost
Python Web Server: http://localhost:8000/
PostgreSQL Server: localhost:5432
Redis Server: localhost:6379
```

**Remind** If you want to change your requirements.txt; should be stopped docker services and then must be executed ```docker-compose build```. Because must be regenerate Python container with new modules.

Finally, if you need to customize, you should browse the src folder.
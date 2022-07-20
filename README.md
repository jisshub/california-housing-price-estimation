# california-housing-price-estimation

## software and account requirements

1. [Github Account](https://github.com/)
2. [Heroku Account](https://dashboard.heroku.com/)
3. [VS Code IDE](https://code.visualstudio.com/)
4. [Git CLI](https://git-scm.com/)

## create conda environment

```sh
conda create -n california-housing-price-estimation python=3.9 -y
```

## To activate this environment, Use command prompt as our shell. then type below command,

```sh
conda activate california-housing-price-estimation
```
## To deactivate an active environment, use

```sh
$ conda deactivate
```

## Create requirments.txt file

### Install packages from requirements.txt

```sh
pip install -r requirements.txt
```
### Save packages to requirements.txt file

```sh
pip freeze > requirements.txt
```
## CI/CD pipeline

To setup CI/CD pipeline in heroku, WE NEED TO GIVE BELOW INFORMATION

1. HEROKU_EMAIL = jissmon476@gmail.com
2. HEROKU_API_KEY = 4712e2b4-2f7b-4a47-b0f5-9b982b47d340
3. HEROKU_APP_NAME = housing-prediction-regression

https://dashboard.heroku.com/account

## Create a Docker File

- Install docker in our system.

Create a file name *Dockerfile* in our root folder.

* Write instructions in Dockerfile to create a Docker image.
    - Give the python version to be used inside our docker machine.
    - virtual environment not needed in our docker machine.
    - No need of git files in our docker machine, so ignore them.
    - Copy the contents to app folder in our docker machine.
    - Change working directory to app folder in our docker machine.
    - Run requirements.txt file in our docker machine.
    - Expose port number which will be sent from environment variable to our docker machine.
    - Launch our applicatioin with help of gunicorn command.

    ```dockerfile
    FROM python:3.9
    COPY . /app
    WORKDIR /app
    RUN pip install -r requirements.txt
    EXPOSE $PORT
    CMD gunicorn --worker=4 --bind 0.0.0.0:$PORT app:app 
    ```


TIME: 1:44:20



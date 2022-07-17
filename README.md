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

1. HEROKU_EMAIL
2. HEROKU_API_KEY
3. HEROKU_APP_NAME

https://dashboard.heroku.com/account

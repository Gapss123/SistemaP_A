curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o miniconda.exe
start /wait "" .\miniconda.exe /S
del miniconda.exe

conda create --prefix .\env python
conda activate .\env

## Instalación de FLASK
pip install flask
pip install "psycopg[binary,pool]"

## Instalación de Flask-SQLAlchemy
pip install flask-sqlalchemy
## Instalación de Flask-WTF
pip install flask-wtf
## Instalación de Flask-Login
pip install flask-login
## Instalación de Flask-Mail
pip install flask-mail

## Instalación de paquetes
pip install -r requirements.txt

# Ejecución en modo desarrollo
conda activate ./env flask --app app run

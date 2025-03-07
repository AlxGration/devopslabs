![CI](https://github.com/AlxGration/devopslabs/actions/workflows/cicd.yml/badge.svg)

# Labs

## Description

The first lab is about to develop and test a simple Python web application, that shows current time in Moscow.

`moscow_time.py` - flask web script
`moscow_time_test.py` - tests

## How to install

#### Install dependencies
```python
pip3 install pytz
pip3 install flask
```

#### Start web server
```bash
export FLASK_APP=moscow_time
export FLASK_ENV=development
flask run
```

#### Guides that used to build the app
1. [First](https://www.digitalocean.com/community/tutorials/how-to-make-a-web-application-using-flask-in-python-3-ru)
2. [Second](https://flask-russian-docs.readthedocs.io/ru/latest/quickstart.html)
3. [Third](https://flask-russian-docs.readthedocs.io/ru/latest/installation.html#installation)


#### Docker

Create image
`docker image build -t <container-name> .`

Run container for test
`docker run --publish 5000:5000 <container-name>`

Publish container to the DockerHub
`docker push <container-name>`


## Testing project

#### Run unit tests

from app_python folder
```bash
python3 -m unittest moscow_time_test
```
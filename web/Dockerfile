# start with a base image
FROM python:3.7

# we use the latest version to avoid issues
RUN python -m pip install --upgrade pip

# all subsequent commands will use this as the default directory
WORKDIR /code

# project dependencies change less often than source code,
# hence the desire to copy `requirements.txt` separately in its own layer
COPY requirements.txt requirements.txt

# install project dependencies
RUN python -m pip install -r requirements.txt

# copy all project files
COPY . .

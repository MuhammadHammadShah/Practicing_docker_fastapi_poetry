FROM ubuntu:22.04
FROM python:3.12
RUN pip install poetry
# create a working dir to work on root dir
WORKDIR /code
# add the current path to docker from pc
ADD ./pyproject.toml  /code/
ADD ./helloworld    /code/helloworld/
RUN poetry install
CMD [ "poetry", "run", "uvicorn", "helloworld.main:app", "--host", "0.0.0.0" ]
FROM python:3.10-slim-buster


# Set the working directory in the container
WORKDIR /backend-flask


# Outsite Container -> Inside Container
COPY requirements.txt requirements.txt


# (Inside Container)Install any needed packages specified in requirements.txt
RUN pip3 install -r requirements.txt


# Outsite Container -> Inside Container
COPY . .


# Define environment variable
ENV FLASK_ENV=development


# CMD (Command)
# Run the command ==> python3 -m flask run --host=0.0.0.0 --port=4567
EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
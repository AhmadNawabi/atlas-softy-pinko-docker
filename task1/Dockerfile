# Using the latest official ubuntu
FROM ubuntu:latest

# Update APT package lists and upgrage existing package with automatic "yes" responce
RUN apt-get update && apt-get upgrade -y

# Install python3, python3-pip and flask
RUN apt-get install -y python3 python3-pip
RUN pip3 install flask

# Set the work directory
WORKDIR /app

# Copy the python file to the working directory in the docker image
COPY api.py /app/

# Expose port 5252 to the host machine
EXPOSE 5252

# Run Python to start the Flask app
CMD ["python3", "api.py"]

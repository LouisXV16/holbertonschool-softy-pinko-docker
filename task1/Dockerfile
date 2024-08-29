# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update the package list for the image
RUN apt-get update

# Upgrade all installed packages to their latest versions
RUN apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Install Flask using pip
RUN pip install Flask

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the local api.py file into the /app directory in the container
COPY ./api.py /app/api.py

# Expose port 5252 for the Flask application
EXPOSE 5252

# Define the command to run the Flask application when the container starts
CMD python3 api.py

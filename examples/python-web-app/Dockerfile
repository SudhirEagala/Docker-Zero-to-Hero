FROM ubuntu:22.04

# Set the working directory in the image
WORKDIR /app

# Copy the files from the host file system to the image file system
COPY . /app

# Install the necessary packages
RUN apt-get update && apt-get install -y python3 python3-pip

# Set environment variable to bypass restriction
ENV PIP_BREAK_SYSTEM_PACKAGES=1

# Copy requirements.txt separately
COPY requirements.txt /app/

# Install Python dependencies
RUN pip install -r requirements.txt

# Set environment variables
ENV NAME World

# Run a command to start the application
CMD ["python3", "app.py","runserver", "0.0.0.0:8000]






# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container at /app
COPY requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the current directory contents into the container at /app
COPY . /app/

EXPOSE 8002

# -u To prevent log accumulation, execute app.py with unbuffered output as soon as the container starts up.
CMD ["python", "-u" ,"app.py"]

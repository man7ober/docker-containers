# Use the official Python image as the base image
FROM python:3.8-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file to the working directory
COPY *.txt .

# Install the dependencies
RUN pip install -r requirements.txt

# Copy the rest of the application source code
COPY . .

# Expose the port that the API listens on
EXPOSE 3002

# Run the Flask application when the container starts
CMD ["python", "inventory_api.py"]
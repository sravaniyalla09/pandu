# Use the official lightweight Python image
FROM python:3.11-slim

# Set environment variables to prevent Python from writing .pyc files 
# and to ensure output is sent straight to terminal (useful for logs)
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory
WORKDIR /code

# Install dependencies first
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY ./app ./app

# Expose the port the app runs on
EXPOSE 8000

# Run the application
CMD ["python", "app/main.py"]

# Use a minimal Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy requirements.txt and devops directory to /app
COPY requirements.txt .
COPY devops/ ./devops/

# Install dependencies
RUN apt-get update && \
    apt-get install -y gcc && \
    pip install --no-cache-dir -r requirements.txt

# Set the default command to run Django development server
CMD ["python", "devops/manage.py", "runserver", "0.0.0.0:8000"]




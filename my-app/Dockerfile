# Base Python
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy dependencies
COPY requirements.txt .

# Install dependencies + gunicorn
RUN pip install --no-cache-dir -r requirements.txt gunicorn

# Copy the rest of the application
COPY . .

# Expose port 80
EXPOSE 80

# Command to run the app
CMD ["gunicorn", "--bind", "0.0.0.0:80", "app.routes:app"]


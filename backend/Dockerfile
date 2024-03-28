# Use the official Python image as base
FROM python:3.8-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the Flask application files into the container
COPY . .

# Install any dependencies specified in requirements.txt, including gunicorn
RUN pip install --no-cache-dir -r requirements.txt gunicorn

# Expose the port on which the Flask app will run
EXPOSE 5000

# Command to run the Flask application using Gunicorn
CMD ["gunicorn", "-b", "0.0.0.0:5000", "server:app"]

FROM python:3.11-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the app directory and requirements.txt into the container
COPY ./app /app/app
COPY ./requirements.txt /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port for the application
EXPOSE 8000

# Run the Uvicorn server
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

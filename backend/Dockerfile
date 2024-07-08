# Use the latest  Python image
FROM python:latest

# Install Node.js 
RUN apt-get update && apt-get install -y \
    nodejs \
    npm

# Install Poetry 
RUN pip install poetry

# Set working dir
WORKDIR /app

# Copy the files
COPY . .

# Install dependencies with Poetry
RUN poetry install

# Expose the port API
EXPOSE 8000

# Run the prestart script and start the server
CMD ["sh", "-c", "poetry run bash ./prestart.sh && poetry run uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload"]
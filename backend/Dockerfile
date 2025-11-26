FROM python:3.11-slim

WORKDIR /app

# Copy requirements first for better caching
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy backend code
COPY . .

# Create data directory
RUN mkdir -p ./data/conversations

# Expose the port
EXPOSE 8001

# Run the application
CMD ["python", "-m", "backend.main"]
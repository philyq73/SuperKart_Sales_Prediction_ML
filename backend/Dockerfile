FROM python:3.9-slim

WORKDIR /app

# Copy frontend requirements
COPY frontend_files/requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy Streamlit application
COPY frontend_files/app.py .

# Start Streamlit
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0", "--server.enableXsrfProtection=false"]

FROM python:3.7-slim-buster


# Working Directory
WORKDIR /app

# Copy source code to working directory
COPY . /app/

# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install  --no-cache-dir --upgrade pip && \
    pip install  --no-cache-dir --trusted-host pypi.python.org -r ./hello_app/requirements.txt

# Expose port 80
EXPOSE 80

# Run app at container launch
CMD ["python", "hello.py"]

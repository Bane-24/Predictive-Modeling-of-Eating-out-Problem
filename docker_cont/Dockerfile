# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory to /app
WORKDIR /app

# Install GDAL dependencies
RUN apt-get update && apt-get install -y \
    libgdal-dev \
    gcc \
    g++ 

# Set GDAL environment variables
ENV CPLUS_INCLUDE_PATH=/usr/include/gdal
ENV C_INCLUDE_PATH=/usr/include/gdal

# Copy the Python script into the container at /app
COPY ./Akshay_u3228988.py /app/Akshay_u3228988.py

# Explicitly copy the data directory with CSV files into the container at /app/data
COPY ./data/ /app/data/

# Install any needed packages specified in requirements.txt
COPY ./requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt


# Command to run the Python script
CMD ["python", "Akshay_u3228988.py"]

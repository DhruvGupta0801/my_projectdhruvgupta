# Python image as the base image (consider version 3.9)
FROM python:3.9

# Set the working directory inside the container as /app
WORKDIR /app

# Copy requirements.txt to the working directory 
COPY requirements.txt ./

# Install project dependencies 
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire project directory into the container
COPY . .

# Expose the port on which the web server will listen
EXPOSE 8080

# Define the command to start the web server
CMD ["flask", "run", "--host=0.0.0.0", "--port=8080"]

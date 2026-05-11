# Get ubuntu image
FROM        ubuntu
#Set working directory as /app folder
WORKDIR     /app
#Install required pyhton librabries
RUN         apt-get update && apt-get install -y python3 python3-pip
#Copy application code to app directory
COPY        requirements.txt .
RUN         pip install --no-cache-dir -r requirements.txt
COPY        . .
WORKDIR     /app/devops
EXPOSE      8000
ENTRYPOINT  ["python3"]
CMD         ["manage.py", "runserver", "0.0.0.0:8000"]




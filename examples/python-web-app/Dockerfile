# Get ubuntu image
FROM        ubuntu
#Set working directory as /app folder
WORKDIR     /app
#Copy application code to app directory
COPY        requirements.txt /app/
COPY        devops  /app/
#Install required pyhton librabries
RUN         apt-get update && apt-get install -y python3 pip
RUN         python3 install requirements.txt && cd devops
EXPOSE      8000
ENTRYPOINT  ["python3"]
CMD         ["manage.py", "runserver", "0.0.0.0:8000"]




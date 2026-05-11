# Get ubuntu image
FROM        ubuntu
#Set working directory as /app folder
WORKDIR     /app
#Install required pyhton librabries
RUN         apt-get update && apt-get install -y python3 python3-pip python3-venv
#For latest ubuntu releases, phython virtual environment is required
RUN         python3 -m venv venv1
ENV         PATH="venv1/bin:$PATH"
#Copy application code to app directory
COPY        requirements.txt .
RUN         pip install --no-cache-dir -r requirements.txt
COPY        . .
WORKDIR     /app/devops
EXPOSE      8000
CMD         ["python", "manage.py", "runserver", "0.0.0.0:8000"]




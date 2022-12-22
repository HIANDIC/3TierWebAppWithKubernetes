FROM python:alpine

# We write the things that will not change first.
COPY requirements.txt .
RUN pip install -r requirements.txt
WORKDIR /app    
# we copy everything from current directory to our image
COPY . .

# run our app after related configuration
CMD ["python", "app.py"]
EXPOSE 80
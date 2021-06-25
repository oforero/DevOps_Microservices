FROM python:3.7.3-stretch

## Step 1:
# Create a working directory
RUN mkdir -p app

## Step 2:
# Copy source code to working directory
WORKDIR /app
COPY requirements.txt .
COPY app.py app.py
COPY model_data model_data

## Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install -r requirements.txt

## Step 4:
# Expose port 80
EXPOSE 80

## Step 5:
# Run app.py at container launch
CMD [ "python", "app.py" ]

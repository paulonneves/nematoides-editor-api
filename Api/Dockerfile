# 
FROM python:3.9

# 
WORKDIR /code

# 
COPY ./requirements.txt /code/requirements.txt

# 
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt
RUN apt-get update && apt-get install -y python3-opencv
RUN pip install opencv-python

# 
COPY ./backend /code/backend

# 
CMD ["uvicorn", "backend.views:app", "--host", "0.0.0.0", "--port", "80"]

## Python 
I created a programming environment for Python. I used the package python:3 directly from Docker hub to set it up. 
On top of that I ran pip upgrade and dependency install commands. I configured CMD to run python interpreter. <br/> 
Docker hub link : https://cloud.docker.com/repository/registry-1.docker.io/purushot/python-env

## Get Python 3
`FROM python:3`

## Run pip upgrade and dependency install command
`pip install --upgrade pip && \` <br/>
`pip install --no-cache-dir nibabel pydicom matplotlib pillow && \` <br/>
`pip install --no-cache-dir med2image` <br/>

## Configure CMD to run python interpreter
CMD ["python3"] 


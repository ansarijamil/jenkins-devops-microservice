FROM python:alpine3.10     
WORKDIR /app   
COPY requirements.txt /app/requirements.txt                           
RUN pip install -r requirements.txt   
EXPOSE 5000  
COPY . /app               
#CMD python ./launch.py     
ENTRYPOINT ["python", "./launch.py"]


#COPY requirements.txt /app/requirements.txt
#ENTRYPOINT ["python", "./launch.py"]


# Explanation of above line of code
 # build application image from base python image
 # speckify working directory
 # will copy all python files from current directory to /app folder
 # using pip to download flask mentioned in requirements.txt vai cmd
 # the port of this container should listen on
# run launch.py application


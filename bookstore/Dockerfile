# The FROM instruction in a Dockerfile specifies the base image for the Docker image being built. 
# the base image we are buildong on top of
FROM python:3.10-slim 

# The WORKDIR instruction in a Dockerfile sets the working directory for any subsequent RUN, CMD, 
# ENTRYPOINT, COPY, and ADD instructions.  

# The working directortty we are building into
WORKDIR /usr/src/app

# The COPY instruction in a Dockerfile is used to copy files and directories from a source location 
# on the host machine (within the build context) to a destination location within the Docker image. 

#Coppy all files form outside the cointener, into the container
COPY . .

# The RUN instruction in a Dockerfile executes commands during the image build process. These 
# commands are used to install software, configure the environment, and perform other tasks needed 
# to prepare the image. Each RUN instruction creates a new layer in the Docker image. 

# Install the python/fastapi dependecies
RUN pip install --no-cache-dir -r requirements.txt

# the EXPOSE the port inside of the docker container
EXPOSE 8000

# The CMD instruction in a Dockerfile specifies the default command to execute when a container starts 
# from the image. It is used to define the main process that will run inside the container. 

# Define the command to rn the Fat API app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]


# Docker
docker build -t name .



docker ps -a

docker rm -f  $(docker ps -qa)


# Dockerfile

# INSTRUCTION	Description
FROM	iIt sets the Base Image for subsequent instructions.
MAINTAINER	It sets the Author field of the generated images.
RUN	It will execute any commands when Docker image will be created.
CMD	It will execute any commands when Docker container will be executed.
ENTRYPOINT	It will execute any commands when Docker container will be executed.
LABEL	It adds metadata to an image.
EXPOSE	It informs Docker that the container will listen on the specified network ports at runtime.
ENV	It sets the environment variable.
ADD	It copies new files, directories or remote file URLs.
COPY	It copies new files or directories.
The differences of [ADD] are that it's impossible to specify remore URL and also it will not extract archive files automatically.
VOLUME	It creates a mount point with the specified name and marks it as holding externally mounted volumes from native host or other containers
USER	It sets the user name or UID.
WORKDIR	It sets the working directory.


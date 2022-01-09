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

# Docker CLI

[lukasz@localhost ~]$ docker

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Options:
      --config string      Location of client config files (default
                           "/home/lukasz/.docker")
  -c, --context string     Name of the context to use to connect to the
                           daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level
                           ("debug"|"info"|"warn"|"error"|"fatal")
                           (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default
                           "/home/lukasz/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default
                           "/home/lukasz/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default
                           "/home/lukasz/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Management Commands:
  app*        Docker App (Docker Inc., v0.9.1-beta3)
  builder     Manage builds
  buildx*     Docker Buildx (Docker Inc., v0.7.1-docker)
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  scan*       Docker Scan (Docker Inc., v0.12.0)
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes

Run 'docker COMMAND --help' for more information on a command.

To get more help with docker, check out our guides at https://docs.docker.com/go/guides/
[lukasz@localhost ~]$ 

-----------------------------------------------------------------------------------------------------------------
# systemctl status docker

[lukasz@localhost ~]$ systemctl status docker
● docker.service - Docker Application Container Engine
   Loaded: loaded (/usr/lib/systemd/system/docker.service; enabled; vendor preset: disabled)
   Active: active (running) since Sat 2022-01-08 22:47:21 PST; 6min ago
     Docs: https://docs.docker.com
 Main PID: 1347 (dockerd)
    Tasks: 10
   Memory: 113.1M
   CGroup: /system.slice/docker.service
           └─1347 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/cont...
[lukasz@localhost ~]$ 








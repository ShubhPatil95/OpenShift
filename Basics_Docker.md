## Docker Basics
#### 1. Create a Dockerfile
- create folder name "Docker" and go inside of it and create a file name "Dockerfile" with below content
```bash
# Use a container with Go pre-installed
FROM quay.io/projectquay/golang:1.17

# Copy our source file into the container
COPY src/hello-world.go /go/hello-world.go

# Set the default environment variables
ENV MESSAGE "Welcome! You can change this message by editing the MESSAGE environment variable."
ENV HOME /go

# Set permissions to the /go folder (for OpenShift)
RUN chgrp -R 0 /go && chmod -R g+rwX /go

# Just documentation.
# This container needs Docker or OpenShift to help with networking
EXPOSE 8080

# OpenShift picks up this label and creates a service
LABEL io.openshift.expose-services 8080/http

# OpenShift uses root group instead of root user
USER 1001

# Command to run when container starts up
CMD go run hello-world.go
```
#### 2. Build image
Make sure you have navigated your shell to folder "Docker"
```ruby
docker build .
```
```ruby
docker images
```
![image](https://github.com/ShubhPatil95/OpenShift/assets/74223025/dd6b2f33-712d-4e4e-9d75-fff2986ff60d)

#### 3. Create Container
```ruby
docker run -it 9c7a54a9a43c
```

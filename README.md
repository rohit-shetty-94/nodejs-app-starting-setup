# **Setup Project (Nodejs + Docker)**

**Created basic nodejs project along with custom Dockerfile**

---

## **Table of Contents**

- [Setup & Installation](#-setup--installation)
- [Dockerfile]
- [Author](#-author)

---

## **Setup & Installation**

### 1️. **Clone the Repository**

```sh
git clone https://github.com/rohit-shetty-94/nodejs-app-starting-setup.git
cd nodejs-app-starting-setup
```

### 2️. **Install Dependencies**

```sh
npm install
```

### 3️. **Build docker image**

```sh
docker build .
```


### 4️. **Publish the port and run docker**

```sh
docker run -p 3000:3000 <docker-id>
```

Server starts at `http://localhost:3000`.

---

## Dockerfile Commands Cheat Sheet

| Command      | Description                                                            | Example                                               |
|--------------|------------------------------------------------------------------------|-------------------------------------------------------|
| **FROM**     | Sets the base image for building the container                          | `FROM golang:1.20`                                     |
| **RUN**      | Executes a command during the build process                             | `RUN go build -o app .`                                |
| **COPY**     | Copies files or directories from the host to the container              | `COPY . /app`                                          |
| **WORKDIR**  | Sets the working directory inside the container                         | `WORKDIR /app`                                         |
| **CMD**      | Specifies the default command to run when the container starts          | `CMD ["./app"]`                                        |
| **ENTRYPOINT** | Configures a container to run as an executable                        | `ENTRYPOINT ["./app"]`                                 |
| **EXPOSE**   | Documents the port the container will listen on                         | `EXPOSE 8080`                                          |
| **ENV**      | Sets environment variables within the container                         | `ENV PORT=8080`                                        |
| **ADD**      | Copies files from the host to the container (supports URLs and archives) | `ADD config.json /app/config.json`                      |
| **VOLUME**   | Creates a mount point and marks it as a volume                          | `VOLUME /data`                                         |
| **LABEL**    | Adds metadata to the image                                              | `LABEL version="1.0" description="My Go App"`           |
| **USER**     | Sets the user to run the container                                       | `USER appuser`                                         |
| **ARG**      | Defines a build-time variable                                           | `ARG VERSION=1.0`                                      |
| **HEALTHCHECK** | Checks the health of a running container                             | `HEALTHCHECK CMD curl --fail http://localhost:8080/health || exit 1` |
| **SHELL**    | Changes the default shell used for the `RUN` command                     | `SHELL ["/bin/bash", "-c"]`                            |




## **Author**

**[Rohit Shetty]**\
🚀 **GitHub**: [rohit-shetty-94](https://github.com/rohit-shetty-94)\
💎 **Email**: [shettyrohit61@gamil.com](mailto\:shettyrohit61@gamil.com)

---



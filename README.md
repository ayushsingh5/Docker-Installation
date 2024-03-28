# Docker-Installation

**Running Linux Containers on macOS with Docker Desktop**

This guide walks you through running Linux containers on your windows and macOS machine using Docker Desktop. Docker provides a convenient way to package and run applications in isolated environments, ensuring consistency and portability across different systems.

**1. Install Docker Desktop**

Docker Desktop is available for both macOS and Windows. Head over to [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/) and download the installer for your operating system. Double-click the downloaded file and follow the on-screen instructions to complete the installation.

**2. Create a Docker Account**

To manage Docker images and repositories, you'll need a free Docker account. Visit [https://hub.docker.com/](https://hub.docker.com/) and sign up for an account. After successful signup, log in using your credentials in the Docker Desktop application.

**3. Choose Recommended Settings**

During installation, Docker Desktop will ask you to choose between recommended and advanced settings. For this guide, we'll stick with the recommended settings, which provide a user-friendly experience for beginners.

**4. Open the Terminal**

- **macOS:**
  - Open **Spotlight** (press Command + Space).
  - Type **Terminal** and press Enter.
- **Windows:**
  - Press the Windows key + R to open the **Run** dialog.
  - Type **cmd** and press Enter.

**5. Pull a Docker Image**

Now that you have a terminal open, we'll use the `docker pull` command to download a pre-built Docker image. Replace `DOCKER_IMAGE_NAME` with the actual name of the image you want to run. For example, to pull an image named `hitheshjithu/test:latest`, you would run:(Note : Replace DOCKER_IMAGE_NAME with the required or suggested Image Name)

```bash
docker pull DOCKER_IMAGE_NAME
```

This command fetches the image from the Docker Hub (a public registry of Docker images) and stores it locally on your machine.

**6. Run the Container**

The `docker run` command starts a container based on the downloaded image. Here's the syntax:

```bash
docker run -p 8888:8888 DOCKER_IMAGE_NAME
```

Let's break down the options:

- `-p 8888:8888`: This maps the container's port 8888 to port 8888 on your macOS host. This allows you to access the application running inside the container from your web browser.
- `DOCKER_IMAGE_NAME`: Replace this with the actual image name you pulled in step 5.

**7. Access the Application**

The terminal output after running the `docker run` command will typically display a URL that includes your machine's IP address and the port (in this case, `http://localhost:8888`). Copy the URL and paste it into your web browser to access the application running within the container.

**Additional Notes:**

- The container will continue to run until you stop it using `docker stop CONTAINER_ID` (where `CONTAINER_ID` is the container's unique identifier).
- To view a list of running containers, use `docker ps`.
- To remove a stopped container, use `docker rm CONTAINER_ID`.

I hope this guide helps you get started with running Linux containers on your macOS as well as windows machine using Docker Desktop!

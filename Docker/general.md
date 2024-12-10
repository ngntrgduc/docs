## General
- Containerization faster than virtualization
- Docker daemon (`dockerd`) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.
- Image contain layers
- Dockerfile $\to$ (docker build) $\to$  Docker image $\to$  (docker run) $\to$ Docker container


## Best practices
- Combine commands: chain commands into one `RUN` command using `&&`, and use `\` to break long commands into multiple lines
- Keep the number of layers low $\to$ smaller image size, improved caching
- Write test script when people are using your image
- Don't install build tools without good reason: Build tools take up a lot of space, and building from source is often slow
- Don't leave temporary files lying around
- Clean up after the package manager
	- If you run `apt-get update` in setting up your container, it populates `/var/lib/apt/lists/` with data that’s not needed once the image is finalized. You can safely clear out that directory to save a few megabytes:
            ```
            RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/*
            ```
- Use environment variables to avoid repeating yourself
- https://docs.docker.com/build/building/best-practices/
	- Use [multi-stage](https://docs.docker.com/build/building/multi-stage/) build

---
Docker security
- https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html
- https://github.com/veggiemonk/awesome-docker#security-1
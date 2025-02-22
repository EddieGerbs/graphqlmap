# GraphQLmap Docker Image

## About
This Docker image provides a stable environment for running [GraphQLmap](https://github.com/swisskyrepo/GraphQLmap). The latest versions of Python cause errors when running GraphQLmap, so this container includes Python 3.6 to ensure compatibility.

## Available Versions
Two versions of the image are available:
- **`python3.6`**: Full Python 3.6 environment with all dependencies.
- **`python3.6-slim`**: A lightweight version with a minimal Python 3.6 installation.

## How to Use

### **1. Pull the Image**
If the image is hosted on GitHub Container Registry (GHCR), you can pull the desired version using:
```sh
# Full version
sudo docker pull ghcr.io/eddiegerbs/graphqlmap/graphqlmap:3.6

# Slim version
sudo docker pull ghcr.io/eddiegerbs/graphqlmap/graphqlmap:3.6-slim
```

### **2. Run GraphQLmap**
To use GraphQLmap, run:
```sh
sudo docker run --rm -it graphqlmap:3.6 graphqlmap --help
```
For an actual scan:
```sh
sudo docker run --rm -it graphqlmap:3.6 graphqlmap -u http://example.com/graphql
```

If using the slim version:
```sh
sudo docker run --rm -it graphqlmap:3.6-slim graphqlmap --help
```

### **3. Run a Bash Shell Inside the Container**
If you need to interact with the container:
```sh
sudo docker run --rm -it graphqlmap:3.6 /bin/bash
```
For the slim version:
```sh
sudo docker run --rm -it graphqlmap:3.6-slim /bin/bash
```

## Notes
- This image is designed for users who want a quick and reliable way to run GraphQLmap.
- It removes the need to manually set up an older Python version.
- The slim version is ideal if you want a smaller, more lightweight container.
- The container is disposable; using `--rm` ensures no leftover data.

Feel free to contribute or report issues!


# GraphQLmap Docker Image

## About
This Docker image provides a stable environment for running [GraphQLmap](https://github.com/swisskyrepo/GraphQLmap). The latest versions of Python cause errors when running GraphQLmap, so this container includes Python 3.6 to ensure compatibility.

## How to Use

### **1. Pull the Image**
The image is hosted on GitHub Container Registry (GHCR), you can pull it using:
```sh
sudo docker pull ghcr.io/eddiegerbs/graphqlmap:3.6
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

### **3. Run a Bash Shell Inside the Container**
If you need to interact with the container:
```sh
sudo docker run --rm -it graphqlmap:3.6 /bin/bash
```

## Notes
- This image is designed for users who want a quick and reliable way to run GraphQLmap.
- It removes the need to manually set up an older Python version.
- The container is lightweight and disposable; using `--rm` ensures no leftover data.

Feel free to contribute or report issues!


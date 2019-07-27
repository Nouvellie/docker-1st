# IMAGES
## What is in an image?

- App binaries and dependencies.
- Metadata about the image data and how to run the image.
- Official definition: "An image is an ordered collection of root filesystem changes and the corresponding execution parameters for use within a container runtime."
- Not a complete OS.
- No Kernelm, or kernel modules. (e.g. drivers)
- Small as one file (your app binary) like a golang static binary.
- Big as a Ubuntu distro with apt, and Apache, PHP, and more installed.

## Link.

- [Docker Hub.](https://hub.docker.com)

## Layers (review)

- Images are made up of file system changes and metadata.
- Each layer is uniquely identified and only stored once on a host.
- This saves storage space on host and transfer time on push/pull.
- A container is just a single read/write layer on top of image.
- "docker image history" and "inspect" commands can teach us.

## Push (only for login user)
#### Push: (user/tag)

```sh
$ docker image push nouvellie/nginx
```
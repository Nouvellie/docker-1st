# DOCKERFILE
## Assignment

- Dockerfiles are part process workflow and part art.
- Take existing Node.js app and Dockerize it.
- Make Dockerfile. Build it, test it, push it (rm it), and run it.
- Expect this to be interactive. Rarely do i get it right the first time.
- Details in "example-1/Dockerfile".
- Use the Alpine version of the official "node" 6.x image.
- Expected result is web site at http://localhost.
- Tag and push to your Docker Hub account. (free)
- Remove your image from local cache, run again from Hub.

## Example1
#### On "example-1" folder:

```sh
$ docker build -t example-1 .
$ docker container run --rm  -p 80:3000 example-1
```
You can build and run the website from this repository locally. If you have Docker installed, there's no need to install and configure mkdocs.

1.Run the following command to build a Docker image for your project:
docker build -t my-mkdocs-image .

This command will use the Dockerfile to create a Docker image with the tag my-mkdocs-image.

2.Once the image has been built, you can run a Docker container from the image with the following command:
docker run -p 8000:8000 -v ${PWD}:/d my-mkdocs-image

This command will start a new container from the my-mkdocs-image image, and bind port 8000 in the container to port 8000 on your local machine. It will also mount the current directory as a volume in the container, so that any changes you make to your MkDocs project on your local machine will be reflected in the container.

You should now be able to view your MkDocs site by navigating to http://localhost:8000 in your web browser.
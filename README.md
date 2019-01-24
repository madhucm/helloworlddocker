# Hello-World

Execute below steps to create docker image and expose as a service.

  - Build Docker image
  ```sh
  docker build -t helloimage -f Dockerfile .
  docker images
  ```
  - Run as a container and map the port (service will run as a deamon)
  ```sh
  docker run -d --name hellocnt -p 7000:80 helloimage
  ```
  - Login to docker
  ```sh
  docker login -u <your docker hub account name>
  ```
  - Create a tag for the image
  ```sh
  docker tag <image_id> <hub account_name>/helloimage:v1
  ```
  - Push image to docker hub
  ```sh
  docker push madhucm/helloimage:v1
  ```
  - Access your service via browser or curl
  http://[ip-of-vm]:7000


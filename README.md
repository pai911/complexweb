# complexweb

A sample project for learning `Docker` & `Docker Compose` with mutiple services based on this [course](https://www.udemy.com/docker-and-kubernetes-the-complete-guide/) on Udemy

## Architecture
![Project Architecture](https://www.lucidchart.com/publicSegments/view/3373a7af-060f-42d5-a9e9-50d763bf7d6f/image.png)
[Diagram](https://www.lucidchart.com/invitations/accept/7938cd15-5ed8-4436-95ce-589702b9fafd)

## Dev
### Config
  - client
    - ./client/Dockerfile.dev
  - nginx
    - ./nginx/Dockerfile.dev
  - server
    - ./server/Dockerfile.dev
  - worker
    - ./worker/Dockerfile.dev
  - Docker Compose: `docker-compose.yml`
### Getting Started
- Use docker-compose to start all containers
  - `docker-compose up --build`
- Nagigate the browser to: http://localhost:3050
- Run Data services inside the containers: 
  - PostgreSQL (Use Docker Hub image)
  - Redis (Use Docker Hub image)

## Production
### Config
  - client
    - ./client/Dockerfile
  - nginx
    - ./nginx/Dockerfile
  - server
    - ./server/Dockerfile
  - worker
    - ./worker/Dockerfile
  - Elastic Beanstalk Docker Config: `Dockerrun.aws.json`
## Getting Started
- Container Deployment: Elastic Beanstalk
  - Config: `Dockerrun.aws.json`
- Use Managed Data services on AWS: 
  - PostgreSQL: AWS RDS
  - Redis: AWS Elastic Cache

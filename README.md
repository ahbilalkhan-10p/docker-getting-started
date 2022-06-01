# Docker Getting Started Tutorial

This tutorial has been written with the intent of helping folks get up and running
with containers and is designed to work with Docker Desktop. While not going too much 
into depth, it covers the following topics:

- Running your first container
- Building containers
- Learning what containers are running and removing them
- Using volumes to persist data
- Using bind mounts to support development
- Using container networking to support multi-container applications
- Using Docker Compose to simplify the definition and sharing of applications
- Using image layer caching to speed up builds and reduce push/pull size
- Using multi-stage builds to separate build-time and runtime dependencies

## Getting Started

If you wish to run the tutorial, you can use the following command after installing Docker Desktop:

```bash
cd app
docker run -d -p 80:80 docker/docker-getting-started
```

Once it has started, you can open your browser to [http://localhost](http://localhost).

## Development

This project has a `docker-compose.yml` file, which will start the mkdocs application on your
local machine and help you see changes instantly.

```bash
docker-compose up
```

To rebuild 
```bash
docker build -t docker-getting-started .
```

start the new container
```bash
docker run -dp 3000:3000 docker-getting-started
```
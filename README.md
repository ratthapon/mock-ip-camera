# Mock IP Camera

## Installation
### Install FFMPEG (Ubuntu)
```
apt-get install ffmpeg
```

### Install Docker, Docker Compose
see [Docker Installation](https://docs.docker.com/engine/install/)

## Deployment
### 1. Prepare data source place video file in `~/data/source.mp4`
or config the volume mapping in docker-compose.yaml

### 2. Deploy services using Docker
All services
```bash
export DOMAIN=test.example.com
docker-compose up -d
```

Only client
```bash
export DOMAIN=test.example.com
docker-compose up -d mock_rtsp_client_stream
```

### 3. (Alternative) Deploy using FFMPEG binary
```bash
source publish_stream.sh
```

## Configurationn
see [FFMPEG](https://ffmpeg.org/ffmpeg.html)

# portainer-cn

portainer-ce 2.11中文版 

[![GitHub Stars](https://img.shields.io/github/stars/outlovecn/portainer-cn.svg?color=94398d&labelColor=555555&logoColor=ffffff&style=for-the-badge&logo=github)](https://github.com/outlovecn/portainer-cn)
[![GitHub Package Repository](https://img.shields.io/static/v1.svg?color=94398d&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=outlovecn&message=GitHub%20Package&logo=github)](https://github.com/outlovecn/portainer-cn/packages)
[![Docker Pulls](https://img.shields.io/docker/pulls/outlovecn/portainer-cn.svg?color=94398d&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=pulls&logo=docker)](https://hub.docker.com/r/outlovecn/portainer-cn)
[![Docker Stars](https://img.shields.io/docker/stars/outlovecn/portainer-cn.svg?color=94398d&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=stars&logo=docker)](https://hub.docker.com/r/outlovecn/portainer-cn)

### 预览
![预览](https://imgs.outlove.cn/dashboard.png)

### 平台支持

支持 `X86`、`ARM`、 `ARM64` 平台的系统

### Docker Hub

`docker pull outlovecn/portainer-cn`
或者
`docker pull ghcr.io/outlovecn/portainer-cn:main`

### 简要说明, 两种使用方式任选其一皆可

1. docker-compose 

```
---
version: "2.1"
services:
  portainer:
    image: outlovecn/portainer-cn:latest
    container_name: portainer
    restart: always
    ports:
      - "9000:9000"
      - "8000:8000"
    volumes:
      - ./dockerconfig/portainer:/data
      - /var/run/docker.sock:/var/run/docker.sock
```

2. docker cli

```
docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data outlovecn/portainer-cn:latest
```


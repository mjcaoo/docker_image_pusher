# Docker Image Pusher

> Original Author: [技术爬爬虾](https://github.com/tech-shrimp/me)
> Video Link: [B站视频](https://www.bilibili.com/video/BV1Zn4y19743/)

## Introduction

使用Github Action自动推送Docker镜像到[阿里云镜像仓库](https://cr.console.aliyun.com/)

## Usage

配置完成后，修改images.txt文件，添加需要推送的镜像名称，每行一个。

每次提交代码，Github Action会自动推送镜像到阿里云镜像仓库。

## Images List

| 镜像名称 | 镜像源 | tag |
| --- | --- | --- |
| nginx | nginx | latest |
| redis | redis | 4.0-alpine |
| postgres | postgres | 10-alpine |
| judge | registry.cn-hongkong.aliyuncs.com/oj-image/judge | 1.6.1 |
| backend | registry.cn-hongkong.aliyuncs.com/oj-image/backend | 1.6.1 |
| openresty | 1panel/openresty | 1.21.4.3-3-3-focal |
| alist | xhofe/alist | v3.37.3 |
| ddns | charles94jp/ddns | latest |
| ros | fishros2/ros | noetic-desktop-full |
| ros | fishros2/ros | humble-desktop-full |
|carla | carlasim/carla | 0.9.15 |

## Tips

- 每次提交，Action会将images.txt文件中的每一条镜像都拉取并推送到阿里云镜像，对于需要最新的镜像很方便，但是对于指定版本的镜像重新拉取并推送是浪费的，故可以将需要的镜像写入images.txt文件，而镜像列表依赖上表维护。
  
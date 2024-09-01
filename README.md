# Docker 镜像地址列表

欢迎来到 **docker-mirror-list** 仓库！本项目致力于收集常用的 Docker 镜像地址，特别是国内镜像，以帮助开发者更方便地获取和使用 Docker 镜像。

## 目录

- [简介](#简介)
- [如何使用](#如何使用)
- [镜像地址列表](#镜像地址列表)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

## 简介

在国内使用 Docker 时，由于网络限制，拉取官方镜像可能速度较慢甚至失败。通过使用镜像源，可以有效提高 Docker 镜像的下载速度。本仓库收集了各大平台和组织提供的镜像地址，以便于开发者根据需要选择使用。

## 如何使用

在您的 Docker 客户端配置中，设置镜像源地址即可。以下是设置 Docker 客户端的步骤，具体操作步骤可能会根据您的操作系统有所差异：

1. 修改 Docker 的配置文件 `daemon.json`：
    - 在 Linux 上通常位于 `/etc/docker/daemon.json` (不存在可自行创建)
    - 在 Windows 上位于 `导航栏设置-侧边栏 Docker Engine`

2. 增加或修改配置项：

```json
{
  "registry-mirrors": [
    "https://your-preferred-mirror.com"
  ]
}
```

3. 重启 Docker 服务以应用更改。

```bash
sudo systemctl daemon-reload
sudo systemctl restart docker
```

原拉取镜像命令：

```bash
docker pull library/alpine:latest
```

加速拉取镜像命令：

```bash
docker pull your-preferred-mirror.com/library/alpine:latest
```

## 镜像地址列表

| 地址 |  提供方  | 说明 |
| ----------- | ----------- | ----------- |
| https://dh-proxy.justcod.ing | 本仓库 | - |
| https://docker.13140521.xyz | imashen | - |
| https://docker.1panel.top | 1Panel 官方 | Cloudflare，国内镜像 |
| https://docker.m.daocloud.io | DaoCloud 官方 | 仅限国内，白名单，阿里云限速 |
| https://docker.1panel.live | 1Panel 官方 | Cloudflare，国内镜像，黑名单 |
| https://proxy.1panel.live | 1Panel 官方 | Cloudflare，国内镜像 |
| https://docker.1panelproxy.com | 1Panel 官方 | Cloudflare，仅限 1Panel 商店应用 |
| https://hub.rat.dev | 耗子面板官方 | Cloudflare |
| https://dockerpull.com | DockerProxy 官方 | Cloudflare |
| https://docker.1panel.dev | 1Panel 核心用户无名驱动 | Cloudflare |
| https://docker.amingg.com | 爱铭网络官方 | Cloudflare |
| https://hub.nat.tf | 棉花云官方 | Cloudflare |
| https://hub1.nat.tf | 棉花云官方 | Nginx |
| https://hub2.nat.tf | 棉花云官方 | Nginx |
| https://docker.1ms.run | 合肥木雷坞官方 | Nginx，国内 CDN，黑名单 |

## 贡献指南

欢迎任何人贡献您的镜像地址和使用经验！请通过提交 Pull Request 的方式贡献，确保提供的信息准确无误。

1. Fork 本仓库
2. 创建新的分支 (git checkout -b feature/new-mirror)
3. 提交您的改动 (git commit -am 'Add a new mirror address')
4. 推送到分支 (git push origin feature/new-mirror)
5. 创建一个新的 Pull Request

## 免责声明

本项目中的所有内容仅供参考，使用本项目提供的信息和服务的风险由用户自行承担。用户在使用过程中应确保遵守所在国家和地区的相关法律法规。我们不对因使用本项目内容而引发的任何直接或间接损失承担责任。使用本项目即表示您同意自行承担可能的风险，并遵守相关法律法规。

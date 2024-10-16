[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
[![GitHub last commit](https://img.shields.io/github/last-commit/Websoft9/docker-library)](https://github.com/Websoft9/docker-library)
[![GitHub Release Date](https://img.shields.io/github/release-date/Websoft9/docker-library)](https://github.com/Websoft9/docker-library)
[![GitHub Repo stars](https://img.shields.io/github/stars/Websoft9/docker-library?style=social)](https://github.com/Websoft9/docker-library)

# 优秀的Docker编写示例

此存储库包括[200+示例](https://github.com/Websoft9/docker-library/tree/main/apps)基于〔Docker
compose〕(https://docs.docker.com/compose/)
例如WordPress、MySQL、Odoo、MongoDB、GitLab、Elastic、Ghost、Grafana、Graylog、Kafka、n8n、Moodle、Nextcloud、ONLYOFFICE、phpMyAdmin。。。
您可以将它们用于业务管理、内容管理、数据分析、开发、DevOps和任何您想做的事情。

## 图像来自哪里？

所有Docker镜像均来自软件官方或权威第三方（如：Bitnami），Websoft9不维护镜像。

Websoft9仅对官方提供的镜像或docker compose进行验证和测试，以确保它们可以直接使用**docker compose up**运行，而无需任何配置。

## 如何使用它？

最简单的方法是安装[Websoft9](https://github.com/Websoft9/websoft9)这可以帮助您在基于web的控制台上运行这些应用程序。

当然，你也可以使用Docker compose来运行这些应用程序：

1.确保你已经安装了最新的Docker，或者你可以通过下面的脚本安装Docker

   ```
   curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && sudo systemctl enable docker && sudo systemctl start docker
   ```

2. 将此存储库下载到您的Linux并列出所有应用程序
   ```
   git clone --depth=1 https://github.com/Websoft9/docker-library
   cd docker-library && ls apps
   ```

3.
转到目标应用程序目录，检查或修改[.env](https://github.com/Websoft9/docker-library/blob/main/docs/code_owner.md#environment-变量），然后运行它

```
# e.g install wordpress
cd apps/wordpress
sudo docker network create websoft9 &&  sudo docker compose up -d
```
4. 添加国内镜像源
```
vim /etc/docker/daemon.json
{
    "registry-mirrors": ["https://docker.m.daocloud.io"]
}
```
目前可用的镜像源：
- https://docker.m.daocloud.io
- https://dockerpull.com
- https://atomhub.openatom.cn
- https://docker.1panel.live
- https://dockerhub.jobcher.com
- https://hub.rat.dev
- https://docker.registry.cyou
- https://docker.awsl9527.cn
- https://do.nark.eu.org/
- https://docker.ckyl.me
- https://hub.uuuadc.top
- https://docker.chenby.cn
- https://docker.ckyl.me

## 如何贡献它？

我们非常欢迎社区为我们的项目提供建议和改进：

1.发现bug，请求功能并提供更好的方法，您可以通过[问题]推广您的想法(https://github.com/Websoft9/docker-library/issues).

2.请按照我们的[贡献指南]（Contributing.md）为这个存储库做出贡献。我们尽最大努力为一些重要任务提供[reward]
（./docs/reward.md）。

## 文档

[Websoft9 Administrator Guide](https://support.websoft9.com/docs/apps)

## 支持

您可以订阅[Weboft9企业支持](https://www.websoft9.com/apps)以确保应用程序的高可用性等：

- 知识：产品专家的答案和指导
- 支持：技术支持所需的一切，例如启用HTTPS、升级指南
- 安全：保护软件的安全服务和工具

## 赞助商

以下公司组织为我们提供了赞助，这极大地帮助了这个存储库。

![image](https://libs.websoft9.com/Websoft9/logo/sponser/50sponser-huawei-logo.png) ![image](https://libs.websoft9.com/Websoft9/logo/sponser/50sponser-mingdaoyun-logo.png) ![image](https://libs.websoft9.com/Websoft9/logo/sponser/50sponser-apitable-logo.png)

## 许可证

[LGPL-3.0](LICENSE.md), 附加条款：未经授权，不得在任何云平台的Marketplace中发布基于此存储库的免费或付费图像。

## 免责声明

我们不能保证开源软件没有漏洞或安全风险，根据开源许可证，这是用户的责任。

## 应用程序愿望清单

提议并投票支持[应用程序]（wishlist.md）打包

## FAQ

#### 我需要在docker编写之前更改密码吗？

是的，您应该在.env文件中修改**W9_POWER_PASSWORD**以用于生产

#### Docker运行失败是因为端口冲突吗？

您应该在.env文件中修改**APP\_\*\_PORT**

#### 申请的资格证书是什么？

W9_LOGIN_USER, W9_LOGIN_PASSWORD

#### 基础设施有限制吗？

不，您可以使用许多基础设施，例如。

- **OS**: Red Hat, CentOS, Debian, Ubuntu or other's Linux OS ...
- **Public Cloud**: More than 20+ major Cloud such as AWS, Azure, Google Cloud, Alibaba Cloud, HUAWEIClOUD, Oracle
  Cloud ...
- **Private Cloud**: KVM, VMware, VirtualBox, OpenStack ...
- **ARCH**: Linux x86-64, ARM 32/64, x86/i686 ...

<!--
 * @Author: tangdaoyong
 * @Date: 2021-01-18 13:54:38
 * @LastEditors: tangdaoyong
 * @LastEditTime: 2021-01-18 14:53:20
 * @Description: podman
-->
# podman

[podman-quickstart](https://blog.websoft9.com/podman-quickstart/)
[Docker Vs Podman](https://zhuanlan.zhihu.com/p/321700587?utm_source=com.microsoft.office.outlook)

## 介绍

Podman 是一个无守护进程的容器引擎，用于在 Linux 系统上进行开发、管理和运行 OCI Containers。 Containers 能以 root 模式运行，也能以非 root 模式运行。
![Podman](./imgs/Podman.png)

Podman 直接与镜像注册表、容器和镜像存储进行交互。
我们知道，Docker 是建立在 [runC 容器运行时](https://www.docker.com/blog/runc/)之上，并且使用了守护进程的; Podman 中没有使用守护进程，而是直接使用 runC 容器运行时。


> Podman 没有守护进程，也不用 REST API 交互，可以使用非 root 模式运行，这便解决了上面提到的 与 Docker 相关的问题 3、4 和 5。

* Podman 不需要启动或管理像 Docker daemon 那样的守护进程。
* 适用于 Docker 的命令在 Podman 中也是同样可用的。您可以指定命令别名：alias docker=podman
* Podman 和 Docker 的镜像具有兼容性
# Ansiban (中文)

**Ansiban** 是一个基于 Ansible 的工具，帮助您快速高效地准备和部署 [Marzban](https://github.com/Gozargah/Marzban)。

## 可用语言

- [中文 (Chinese)](README.ch.md) ✅
- [English](https://github.com/mohrezfadaei/ansiban)
- [فارسی (Persian)](README.fa.md)

## 快速开始

要开始使用 Ansiban，请按以下步骤操作：

### 1. 更新库存文件

修改库存文件 [`hosts.ini`](inventory/hosts.ini) 以包括您的 master 和节点配置：

- **节点名称**：您可以重命名节点（例如 `node1`、`node2`、`node3`）为自定义名称，如 `germany1`。（可选）
- **`ansible_host`**：设置为您服务器的 IP 地址，以便通过 SSH 连接。（必填）
- **`ansible_user`**：指定您用于 SSH 访问的用户名。（必填）
- **`ansible_ssh_private_key_file`**：提供 SSH 私钥的路径，以便访问服务器。（必填）

### 2. 配置 Master 变量

编辑 [`master.yml`](group_vars/master.yml) 文件以自定义 Marzban 的部署：

- **`marzban_subscription_subdomain`**：设置为您的 Marzban 面板子域名（仅应为子域部分，而不是整个域名）。（必填）

    > 例子：
    >
    > ✅ `sub`
    >
    > ❌ `sub.mydomain.com`

- **`marzban_domain`**：指定您的 Marzban 部署的域名（例如 `mydomain.com`）。（必填）
- **`marzban_sub_profile_title`**：为您的组织或子配置文件设置标题。（可选）
- **`db_general_password`**：提供 MySQL 数据库的密码。（必填）

## 致谢

特别感谢 [Marzban](https://github.com/Gozargah/Marzban) 的创建者，他们的开源项目激发了此工具的灵感。

我们还要感谢 Ansible 社区的出色文档和支持，它们在 **Ansiban** 的开发中起到了重要作用。

## 许可证

此项目基于 Apache 2.0 许可证发布。
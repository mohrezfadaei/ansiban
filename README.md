# Ansiban

**Ansiban** is an Ansible-based tool that helps you prepare and deploy [Marzban](https://github.com/Gozargah/Marzban) quickly and efficiently.

## Available Languages

- [English](https://github.com/mohrezfadaei/ansiban) ✅
- [فارسی (Persian)](README.fa.md)
- [中文 (Chinese)](README.ch.md)

## Quick Start

To get started with Ansiban, follow these simple steps:

### 1. Update the Inventory File

Modify the inventory file [`hosts.ini`](inventory/hosts.ini) to include your master and node configurations:

- **Node Names**: You can rename nodes (e.g., `node1`, `node2`, `node3`) to custom names such as `germany1`. (Optional)
- **`ansible_host`**: Set this to your server's IP address for SSH connections. (Required)
- **`ansible_user`**: Specify the username you use for SSH access. (Required)
- **`ansible_ssh_private_key_file`**: Provide the path to your SSH private key for server access. (Required)

### 2. Configure the Master Variables

Edit the [`master.yml`](group_vars/master.yml) file to customize the Marzban deployment:

- **`marzban_subscription_subdomain`**: Set this to your Marzban panel subdomain (this should be only the subdomain part, not the full domain). (Required)

    > Example:
    >
    > ✅ `sub`
    >
    > ❌ `sub.mydomain.com`

- **`marzban_domain`**: Specify the domain name for your Marzban deployment (e.g., `mydomain.com`). (Required)
- **`marzban_sub_profile_title`**: Set the title for your organization or sub-profile. (Optional)
- **`db_general_password`**: Provide the password for the MySQL database. (Required)

## Acknowledgements

Special thanks to the creators of [Marzban](https://github.com/Gozargah/Marzban) for their open-source project, which inspired this tool.

We would also like to express our gratitude to the Ansible community for their excellent documentation and support, which has been instrumental in the development of **Ansiban**.

## License

This project is licensed under the Apache License, Version 2.0.

# InstallNET.sh 自动安装脚本

## 📌 脚本来源
本脚本来源于 **MoeClub**，用于通过网络自动安装 Debian、Ubuntu 或 CentOS 系统。

为了方便使用，本仓库会每天自动拉取最新的 `InstallNET.sh` 版本，并存储在 GitHub。

**原始脚本地址**：

```
https://moeclub.org/attachment/LinuxShell/InstallNET.sh
```


## 🚀 使用方法
可以通过 `wget` 或 `curl` 下载并执行脚本：

### **方式 1：使用 `wget`**
```bash
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/youwodev/InstallNET/main/InstallNET.sh') -d 12 -v 64 -a
```

### **方式 2：使用 `curl`**
```bash
curl -fsSL 'https://raw.githubusercontent.com/youwodev/InstallNET/main/InstallNET.sh' | bash -s -- -d 12 -v 64 -a
```

## 🛠 默认参数解释
```bash
bash InstallNET.sh -d 12 -v 64 -a
```
- `-d 12`  → 选择 **Debian 12**
- `-v 64`  → 选择 **64 位系统**（amd64）
- `-a`     → **自动安装模式**（无需人工干预）

## ⚙ 可用参数列表
脚本支持多种参数，可用于不同系统的安装：

| 参数 | 说明 | 示例 |
|------|------|------|
| `-d` 或 `--debian` | 选择 Debian 版本 | `-d 12`（Debian 12） |
| `-u` 或 `--ubuntu` | 选择 Ubuntu 版本 | `-u 20.04`（Ubuntu 20.04） |
| `-c` 或 `--centos` | 选择 CentOS 版本 | `-c 7`（CentOS 7） |
| `-v` 或 `--ver` | 指定架构（32/64位） | `-v 64`（amd64） |
| `-p` 或 `--password` | 设置 root 密码 | `-p "YourPassword"` |
| `-i` 或 `--interface` | 指定网络接口 | `-i eth0` |
| `--ip-addr` | 设置静态 IP 地址 | `--ip-addr 192.168.1.100` |
| `--ip-mask` | 设置子网掩码 | `--ip-mask 255.255.255.0` |
| `--ip-gate` | 设置默认网关 | `--ip-gate 192.168.1.1` |
| `--ip-dns` | 设置 DNS 服务器 | `--ip-dns 8.8.8.8` |
| `-port` | 指定 SSH 端口 | `-port 2222` |
| `--mirror` | 指定安装源镜像 | `--mirror "http://deb.debian.org/debian"` |
| `-dd` 或 `--image` | 使用 `dd` 方式安装 Windows | `-dd "http://example.com/windows.img.gz"` |


## ⚠ 注意事项
1. **请确保数据已备份**，此脚本会格式化硬盘并安装新系统。
2. **如果使用 `-dd` 模式安装 Windows，请确认 `DDURL` 可信**，避免恶意系统。
3. **默认 SSH 端口为 `22`，可使用 `-port` 参数修改**。

## 📜 许可证
本脚本原始作者为 **MoeClub**，请尊重原作者版权。本仓库仅用于自动同步脚本，不对其内容负责。

---

📢 **本仓库每日自动更新 `InstallNET.sh`，如果你想获取最新版本，可以直接从此仓库下载！** 🚀


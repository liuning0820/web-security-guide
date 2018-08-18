# NMAP 学习

nmap是一个网络连接端扫描软件，用来扫描网上电脑开放的网络连接端。确定哪些服务运行在哪些连接端，并且推断计算机运行哪个操作系统（这是亦称 fingerprinting）。它是网络管理员必用的软件之一，以及用以评估网络系统安全。

https://nmap.org

## NMAP用途

- 通过对设备或者防火墙的探测识别来审计它的安全性。
- 端口扫描：探测目标主机所开放的端口和系统信息。
- 网络存储，网络映射，维护和资产管理。（这个有待深入）
- 主机探测: 查看网络里哪些设备是开机着的。

## 实例

- 主机探测

    ```sh
    nmap -sn 192.168.1.0-225
    nmap -sP 192.168.0.1-225
    ```

- 端口扫描

    ```sh
    nmap –A 192.168.229.134
    nmap –O 192.168.229.134

    <!-- 扫描IP 192.168.1.100 中开放的端口，并找出哪些服务对应这些端口 -->
    nmap -PN -sT -sV -p0-65535 192.168.1.100

    # Read list of hosts/networks from a file (IPv4)
    nmap -iL /tmp/test.txt
    # Excluding hosts/networks
    nmap 192.168.1.0/24 --exclude 192.168.1.5
    nmap 192.168.1.0/24 --exclude 192.168.1.5,192.168.1.254
    nmap -iL /tmp/scanlist.txt --excludefile /tmp/exclude.txt

    ```

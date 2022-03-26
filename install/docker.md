# docker
doc

https://docs.docker.com/engine/install/ubuntu/#os-requirements


# 解决docker 日志文件过大的问题
## 修改daemon.json
```bash
$ nano /etc/docker/daemon.json
{
  "log-driver": "json-file",
  "log-opts": {
    "max-size": "50m",
    "max-file": "3"
  }
}

$ systemctl daemon-reload
# 重启docker守护进程
$ systemctl restart docker
```
## 163 网易云镜像 配置
```
/etc/docker/daemon.json
{
  "registry-mirrors": ["http://hub-mirror.c.163.com"],
  "log-driver": "json-file",
  "log-opts": {
    "max-size": "50m",
    "max-file": "3"
  }
}
```
## 已有日志清理
```bash
$ sudo du -d1 -h /var/lib/docker/containers | sort -h
# 对已有日志排序
$ sudo echo "" > log_file.log
# 清空已有日志
```

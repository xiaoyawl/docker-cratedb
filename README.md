# docker-cratedb

## 使用方法:
### 1: 调整内核参数
```bash
echo 'vm.max_map_count=655360' >> /etc/sysctl.conf && sysctl -p
```
### 2：创建自定义配置文件
```bash
mkdir -p /data/CrateDB/config
curl -Lk https://github.com/xiaoyawl/docker-cratedb/raw/master/crate.yml > /data/CrateDB/config/crate.yml
```
### 3: 配置docker-compose文件
```bash
curl -Lk https://github.com/xiaoyawl/docker-cratedb/raw/master/docker-compose.yml > /data/docker-compose.yml
```
### 4: 启动容器
```bash
docker-compose -f /data/docker-compose.yml up -d
```

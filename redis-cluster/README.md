apt-get update
apt install net-tools

redis-cli --cluster create --cluster-replicas 1 192.168.65.3:6379 192.168.65.3:6380 192.168.65.3:6381 192.168.65.3:6382 192.168.65.3:6383 192.168.65.3:6384
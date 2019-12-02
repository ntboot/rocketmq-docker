使用动态pv
将entrypoint.sh 同步至node 的/opt/rocketmq-4.3.1/bin/目录下

执行脚本前，先创建命名空间：

```bash
kubectl create namespace rocketmq
kubectl label nodes kube04 node-role.kubernetes.io/rocketmq=true
kubectl label nodes kube05 node-role.kubernetes.io/rocketmq=true
kubectl apply -f rocketmq-broker-storageclass.yaml
```

# CUDCOS_containerization_of_hadoop_cluster
hadoop平台集群容器化

Tutorial:

一、制作镜像

1. 运行img/yarn/build.sh制作dockerfile

二、环境准备

1. 在主节点上运行 img/yarn/master_bootstrap.sh

2. 在从节点上运行 img/yarn/agent_bootstrap.sh

三、使用kubernetes拉起镜像
`"
kubectl create -f yarn_master-service.yaml

kubectl create -f yarn_master-controller.yaml

kubectl create -f yarn_agent-controller.yaml
`"

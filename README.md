<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fahpeng%2FDockerSwarmMode%2Fmaster%2Fazuredeploymooncake.json" target="_blank">
    <img src="https://raw.githubusercontent.com/ahpeng/DockerSwarm/master/images/azuremooncake.png"/>
</a>
<a href="https://portal.azurestack.local/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fahpeng%2FDockerSwarmMode%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/ahpeng/DockerSwarm/master/images/azureStack.png"/>
</a>

# 在Azure中国和Azure Stack部署Docker Swarm Mode Cluster

参考以下文档：

https://github.com/Azure/acs-engine/blob/master/docs/swarmmode.md

Azure Stack的ARM模板参考以下：

https://github.com/Azure/azure-quickstart-templates/tree/master/101-acsengine-swarmmode

Azure中国区的ARM模板直接用ACS-Engine生成，支持虚拟机扩展集和托管磁盘。

=======
对Azure Stack模板作了以下修改：

1. Azure Stack模板修改了VM Image参数和API版本、以及Custom Script for Linux的VM扩展版本参数。


2. 修改CustomData部分，以便使用ACS-Engine的最新configure-swarmmode-cluster.sh脚本。以确保安装稳定的docker 17.03版本，以避免出现docker daemon无法启动的问题

欢迎关注微信公众号：sysinternal，欢迎加我们微信群：markpah   

可以同时在中国区Azure和Azure Stack上部署。

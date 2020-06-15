## 文件功能

### Dockerfile

1. 安装jdk8;
2. 下载安装hadoop;
3. 配置环境变量;
```shell script
PATH
JAVA_HOME
HADOOP_HOME
HADOOP_CONF_DIR
MULTIHOMED_NETWORK=1    # 多链路接入cluster nodes are connected to more than one network interface
USER
```
4. 启动entrypoint.

### entrypoint.sh

1. 配置服务 `/etc/hadoop`

| 配置文件(配置模块) | 配置选项 | 功能 |
|--|--|--|
| core-site.xml   | CORE_CONF | |
| hdfs-site.xml   | HDFS_CONF | |
| yarn-site.xml   | YARN_CONF | |
| httpfs-site.xml | HTTPFS_CONF| |
| kms-site.xml    | KMS_CONF   | |
| mapred-site.xml | MAPRED_CONF| |


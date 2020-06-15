## 端口

## 共有的配置

| 配置模块 | 配置KEY | 配置VALUE | 功能 |
|--|--|--|--|
| core-site.xml | hadoop.proxyuser.hue.hosts | * |
|               | fs.defaultFS               | hdfs://namenode:9000 |
|               | hadoop.http.staticuser.user| root |
|               | io.compression.codecs      | org.apache.hadoop.io.compress.SnappyCodec |
|               | hadoop.proxyuser.hue.groups| * |
| hdfs-site.xml | dfs.namenode.datanode.registration.ip-hostname-check | false |
|               | dfs.webhdfs.enabled        | true |
|               | dfs.permissions.enabled    | false |
|               | dfs.namenode.name.dir      | file:///hadoop/dfs/name |
| yarn-site.xml | yarn.timeline-service.enabled | true |
|               | yarn.scheduler.capacity.root.default.maximum-allocation-vcores | 4
|               | yarn.resourcemanager.system-metrics-publisher.enabled | true
|               | yarn.resourcemanager.store.class | org.apache.hadoop.yarn.server.resourcemanager.recovery.FileSystemRMStateStore
|               | yarn.nodemanager.disk-health-checker.max-disk-utilization-per-disk-percentage | 98.5
|               | yarn.log.server.url | http://historyserver:8188/applicationhistory/logs/
|               | yarn.resourcemanager.fs.state-store.uri | /rmstate
|               | yarn.timeline-service.generic-application-history.enabled | true
|               | yarn.log-aggregation-enable | true
|               | yarn.resourcemanager.hostname | resourcemanager
|               | yarn.scheduler.capacity.root.default.maximum-allocation-mb | 8192
|               | yarn.nodemanager.aux-services | mapreduce_shuffle
|               | yarn.resourcemanager.resource_tracker.address | resourcemanager:8031
|               | yarn.timeline-service.hostname | historyserver
|               | yarn.resourcemanager.scheduler.address | resourcemanager:8030
|               | yarn.resourcemanager.address | resourcemanager:8032
|               | mapred.map.output.compress.codec | org.apache.hadoop.io.compress.SnappyCodec
|               | yarn.nodemanager.remote-app-log-dir | /app-logs
|               | yarn.resourcemanager.scheduler.class | org.apache.hadoop.yarn.server.resourcemanager.scheduler.capacity.CapacityScheduler |
|               | mapreduce.map.output.compress | true |
|               | yarn.nodemanager.resource.memory-mb | 16384 |
|               | yarn.resourcemanager.recovery.enabled | true |
|               | yarn.nodemanager.resource.cpu-vcores | 8 |
| httpfs-site.xml | | |
| kms-site.xml | | |
| mapred-site.xml | mapreduce.map.java.opts | -Xmx3072m
|               | mapreduce.reduce.memory.mb | 8192
|               | mapreduce.reduce.java.opts | -Xmx6144m
|               | yarn.app.mapreduce.am.env | HADOOP_MAPRED_HOME=/opt/hadoop-3.2.1/
|               | mapreduce.map.memory.mb | 4096
|               | mapred.child.java.opts | -Xmx4096m
|               | mapreduce.reduce.env | HADOOP_MAPRED_HOME=/opt/hadoop-3.2.1/
|               | mapreduce.framework.name | yarn
|               | mapreduce.map.env | HADOOP_MAPRED_HOME=/opt/hadoop-3.2.1/




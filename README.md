# elasticsearch-with-ik

该elasticsearch中预装ik，并已配置搜狗词库

### 版本


| Elasticsearch version | IK version            |
| ----------------------| ----------------------|
| 2.3.4                 | 1.9.4                 |    

### 安装运行

 - 安装

下载解压并命名为elasticsearch到/opt/目录下

 - 运行

```bash
cd /opt && ./elasticsearch/bin/elasticsearch

```

### 使用

新建一个名为libraray的索引

```bash
# number_of_shards 分片数
# number_of_replicas 副本数
PUT /library
{
    "settings": {
        "index": {
            "number_of_shards": 5,
            "number_of_replicas": 1
        }
    }
}

```
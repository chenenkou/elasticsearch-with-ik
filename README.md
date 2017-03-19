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

### Head插件安装

在 elasticsearch/bin 目录下执行下面的命令：
```
plugin install mobz/elasticsearch-head
```
安装成功后，启动 Elasticsearch, 然后在浏览器中输入：
```
http://127.0.0.1:9200/_plugin/head/
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
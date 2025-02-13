# Apache Zeppelin on Staroid ⭐


[Apache Zeppelin](https://zeppelin.apache.org) on [Staroid](https://staroid.com).

**Documentation:** [User Guide](https://zeppelin.apache.org/docs/latest/index.html)<br/>
**Mailing Lists:** [User and Dev mailing list](https://zeppelin.apache.org/community.html)<br/>
**Continuous Integration:** ![core](https://github.com/apache/zeppelin/workflows/core/badge.svg) ![frontend](https://github.com/apache/zeppelin/workflows/frontend/badge.svg) ![rat](https://github.com/apache/zeppelin/workflows/rat/badge.svg) <br/>
**Contributing:** [Contribution Guide](https://zeppelin.apache.org/contribution/contributions.html)<br/>
**Issue Tracker:** [Jira](https://issues.apache.org/jira/browse/ZEPPELIN)<br/>
**License:** [Apache 2.0](https://github.com/apache/zeppelin/blob/master/LICENSE)
>>>>>>> 06e7a341798a8ba152432397efbe3155e53c4f5b

[![Run](https://staroid.com/api/run/button.svg)](https://staroid.com/api/run)

## Key features 🚀


- Latest version

Core features:
   * Web based notebook style editor.
   * Built-in Apache Spark support
>>>>>>> 06e7a341798a8ba152432397efbe3155e53c4f5b

    Access the latest features and improvements on the Apache Zeppelin, in a single click!
    No need to install or maintain Zeppelin to keep it up-to-dated.

    Markdown, Shell, Spark, Python, JDBC interpreters are included

- Kubernetes mode (== Scalable)

    Zeppelin on Kubernetes is enabled by default. Each interpreter runs on their own container.

- Spark 3.0

<<<<<<< HEAD
    Comes with Spark 3.0.

- Zero maintenance Spark Cluster

    It configures Spark on Kubernetes out of the box.
    That means you don't need to configure, manage Spark cluster. Instead, just give number of executors you want in the notebook and enjoy distributed computing without headache.


    ```
    %spark.conf
    spark.executor.instances 3

    %spark
    // run spark API. 3 instances of worker will be automatically created
    ```

    <img src="https://user-images.githubusercontent.com/1540981/80290438-cf3bc180-86f9-11ea-8c1f-d2dedcd48a86.png" width="700px" />

- Spark UI access

    Open Spark UI from the notebook and get more insight
    
    <img src="https://user-images.githubusercontent.com/1540981/80290443-d8c52980-86f9-11ea-999c-eeafab25cf38.png" width="700px" />
    

- File manager

    You can upload/download file and access them in `/data` directory from the interpreter.
    <img src="https://user-images.githubusercontent.com/1540981/82079532-d79f7080-9697-11ea-99c5-5787f070dce9.gif" width="500px"/>


- Customize your self.

    Fork this repository and launch your customized version on [Staroid](https://staroid.com). No complex setup required. Just connect your forked Github repository and push commits.


## Spark configuration

Driver and executors can be configured using conf interpreter

```
%spark.conf
spark.driver.cores                                            2
spark.driver.memory                                           8g
spark.executor.cores                                          4
spark.executor.memory                                         16g
spark.executor.instances                                      3
spark.kubernetes.executor.label.pod.staroid.com/isolation     dedicated
spark.kubernetes.executor.label.pod.staroid.com/instance-type standard-4
spark.kubernetes.executor.label.pod.staroid.com/spot          true
```

### TestDrive

TestDrive namespace quota is smaller. So need to use smaller cores and memory.

```
%spark.conf
spark.driver.cores                                            1
spark.driver.memory                                           1g
spark.executor.cores                                          1
spark.executor.memory                                         1g
```


## Branch

| Branch | Zeppelin version |
| ------ | --------------- |
| master-snapshot | latest master |


## Development

Feedbacks and Pull Requests are welcome.
This repository only edits `.staroid` directory. For the update on any other files, please make a PullRequest to [Apache Zeppelin upstream repository](https://github.com/apache/zeppelin) directly.

Check out [.staroid](https://github.com/open-datastudio/zeppelin/tree/master-snapshot/.staroid) directory of `master-snapshot` branch to learn how it made Zeppelin on Staroid.


| contents | description |
| -------- | ----------  |
| staroid.yaml | [staroid config](https://docs.staroid.com/references/staroid_yaml.html) file |
| skaffold.yaml | skaffold config file |
| conf | Zeppelin configuration files to override |
| docker | Dockerfile to build images |
| k8s | Kubernetes resource manifests |


### Run locally with prebuilt image

It takes 30~40 minutes to build all images while Zeppelin requires long time to build.
`prebuilt` profile is included in skaffold.yaml so changes doesn't necessary to re-build Zeppelin can be tested quickly in local minikube environment.

```
skaffold dev -f .staroid/skaffold.yaml -p prebuilt,minikube --port-forward
```
=======
### Build from source
Please check [Build from source](https://zeppelin.apache.org/docs/latest/setup/basics/how_to_build.html) to build Zeppelin from source.
>>>>>>> 06e7a341798a8ba152432397efbe3155e53c4f5b

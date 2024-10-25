<!---
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# hbase-connectors

Connectors for [Apache HBase&trade;](https://hbase.apache.org)

* [Kafka Proxy](https://github.com/apache/hbase-connectors/tree/master/kafka)
* [Spark](https://github.com/apache/hbase-connectors/tree/master/spark)


# Sprout

Yes, this is a clone of a public repo.  Yes, this is important and used in both listening and DFZ zones.

Why Does this exist?  Simple: the hadoop ecosystem is a dependency nightmare.

Keeping up with security patches is a non starter is many cases.

# How to test

In `./spark/pom` update this line:
```
<protocArtifact>com.google.protobuf:protoc:${external.protobuf.version}:exe:${os.detected.classifier}</protocArtifact>
```

To Be this instead
```
<protocArtifact>com.google.protobuf:protoc:${external.protobuf.version}:exe:osx-x86_64</protocArtifact>
```

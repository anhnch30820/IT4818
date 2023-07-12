# Build Image
- Build base image:
`cd base`
`docker build -t bim8192/hadoop-base:3.2.1 .`

- Build namenode image:
`cd namenode`
`docker build -t bim8192/hadoop-namenode:3.2.1 .`

- Build datanode image:
`cd datanode`
`docker build -t bim8192/hadoop-datanode:3.2.1 .`
';
# Copy file txt sample vào container
`docker cp <path file txt> <namenode id>:/opt`

# Upload and delete txt file to HDFS
`hadoop fs -mkdir hdfs://namenode:9000/week_1`
`hadoop fs -put /opt/test.txt hdfs://namenode:9000/week_1`
`hadoop dfs -rm -R hdfs://namenode:9000/week_1/test.txt`
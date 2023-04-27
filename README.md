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

# Copy file txt sample vào container
`docker cp <path file txt> <namenode id>:/opt`

# Upload txt file to HDFS
`hadoop fs -mkdir hdfs://namenode:9000/week_1`
`hadoop fs -put /opt/sample3.txt hdfs://namenode:9000/week_1`
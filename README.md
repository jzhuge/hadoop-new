# Hadoop Bash Automated Tests

Only support HDFS, DistCp, HttpFS, and KMS for now.

## Install Bats

* [Bats: Bash Automated Testing System](https://github.com/sstephenson/bats)

## Start Hadoop in pseudo-distributed mode

    pseudo_dist start unsecure|ssl

## Stop Hadoop in pseudo-distributed mode

    pseudo_dist kill|stop

## Run all tests

    bats scripts

## Run KMS tests

    bats scripts/kms.bats

## Run HttpFS tests

    bats scripts/httpfs.bats

## Environment variables

Name             | Description
-----------------|-------------
HADOOP_HOME      | Hadoop home directory
HADOOP_CONF_DIR  | Hadoop config directory
TEST_HOST        | The host where Hadoop is running
TEST_HTTPFS_PORT | HttpFS port
TEST_KMS_PORT    | KMS port
TEST_SERVICES    | Space delimited list of Hadoop services: hdfs, distcp, httpfs, and kms

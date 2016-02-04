# AWS CLI in Docker

This is containerized AWS CLI on alpine to avoid requiring the aws cli to be installed on CI machines.


## Build

```
cd <repo>/build/aws-cli
docker build -t mesosphere/aws-cli .
```


## Usage

Configure:

```
export AWS_ACCESS_KEY_ID="<id>"
export AWS_SECRET_ACCESS_KEY="<key>"
```

Upload file to S3:

```
./aws.sh s3 cp ../dcos-centos-virtualbox-0.2.1.box s3://dcos-vagrant/
```


AWS CLI Docs: https://aws.amazon.com/documentation/cli/
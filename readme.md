# Docker Notes

Docker works ??

Docker vs VM

Image vs Container

## Guides

- Images and containers

```

docker run -it -p a:b -d  node

docker ps -a

docker build .

```

# Transferring file from local to aws instances

https://dearsikandarkhan.medium.com/files-copying-between-aws-ec2-and-local-d07ed205eefa
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html
https://stackoverflow.com/a/21279678/12210002
https://stackoverflow.com/a/34935676/12210002

- Copying files from EC2 to local

```
scp -i /directory/to/abc.pem user@ec2-xx-xx-xxx-xxx.compute-1.amazonaws.com:path/to/file /your/local/directory/files/to/download
                                                               -------------------------
```

- Copying files from local to EC2

```
scp -i /directory/to/abc.pem /your/local/file/to/copy user@ec2-xx-xx-xxx-xxx.compute-1.amazonaws.com:path/to/file
                                           ----------                                          -------------
```

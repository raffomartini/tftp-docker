# tftp-docker
tftp server for Docker

```
docker build --rm --tag=rmartini/tftp .
```

To run and mount the `/opt/tftpboot` as tftp folder:
```
docker run -p 0.0.0.0:69:69/udp -v /opt/tftpboot:/var/tftpboot -i -t rmartini/tftp
```

Note: 
doesn't work on MAC, troubleshooting, I can access tftp from within the container, it wuould seems an issue with port forwarding.

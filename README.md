Docker file for Logitech Media Server/Squeezeboxserver on CentOS 6  
Run:
```
docker run -d \
        -v /etc/localtime:/etc/localtime
	-p 3483:3483/udp \
	-p 3483:3483/tcp \
	-p 9000:9000 \
	-p 9090:9090 \
	-v <local_state_dir>:/mnt/state \
	-v <local_music_dir>:/mnt/music \
	-v /etc/localtime:/etc/localtime \
	twobaker/squeezeboxserver
```

You can find logs and preferences in \<local_state_dir\>. To prevent clashing with user IDs on the host server, Squeezeboxserver runs with UID 8888 and GID 8888.


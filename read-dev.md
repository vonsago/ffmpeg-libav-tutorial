//  vonsago/ffmpeg-devel with vim

```shell script
docker run -w /files --rm -it -v `pwd`:/files vonsago/ffmpeg-devel bash
```

compile:
```shell script
gcc -L/opt/ffmpeg/lib -I/opt/ffmpeg/include/ /files/0_hello_world.c \
 	  -lavcodec -lavformat -lavfilter -lavdevice -lswresample -lswscale -lavutil \
 	  -o /root/hello
```
run:
```shell script
/root/hello /files/small_bunny_1080p_60fps.mp4
```
result: `ls`


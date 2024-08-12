# MotionEye
MotionEye | Tu CCTV en Docker
![motioneye-featured-image-new](https://github.com/user-attachments/assets/4f15f18c-d64b-4dc0-af94-4ac05d53b587)

### MotionEye OS
https://github.com/ccrisan/motioneye

Go to release page, https://github.com/ccrisan/motioneye/releases, download a release and burn it to your device.

### MotionEye on Docker
https://github.com/ccrisan/motioneye/wiki/Install-In-Docker

docker run --name="motioneye" \
    -p 8765:8765 -p 8081:8081\
    --hostname="motioneye" \
    -v /etc/localtime:/etc/localtime:ro \
    -v /etc/motioneye:/etc/motioneye \
    -v /var/lib/motioneye:/var/lib/motioneye \
    --restart="always" \
    --detach=true \
    --device=/dev/video0 \
    ccrisan/motioneye:master-armhf

Add -p 8081:8081 for streaming
Add --device=/dev/video0 for camera

List CAM

ls /dev | grep video

### MotionEye docker-compose.yml
-> https://github.com/JLalib/docker-motioneye/blob/main/docker-compose.yml

### Default Credentials
username: "admin"

password: ""

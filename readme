 docker build -t="frps" .
 docker build -t="frpc" .



docker run --restart always -itd --name frps  --hostname frps -p 80:80 -p 443:443 -p 7000:7000 -p 7500:7500  -p 5900:5900 -v /root/docker-frp:/opt/frp  frps
docker run --restart always -itd --name frpc  --hostname frpc -v /root/docker-frp:/opt/frp  frpc

docker build -t="frps" .
docker build -t="frpc" .

cd ~;git clone https://github.com/w796933/xiang_docker_frp.git

docker run --restart always -itd --name frps --hostname frps -p 80:80 -p 443:443 -p 7000:7000 -p 7500:7500 -p 3389:3389 -p 5900:5900 -v /root/xiang_docker_frp/conf:/opt/frp/conf w796933/docker_frp_xiang:frps

frpc running

docker run --restart always -itd --name frpc --hostname frpc -v /root/xiang_docker_frp/conf:/opt/frp/conf w796933/docker_frp_xiang:frpc

# mynewtest
```
docker version
 1640  sudo docker version
 1641  docker version
 1642  su - u3
 1643  sudo su - u3
 1644  docker images
 1645  docker run alpine date
 1646  date
 1647  docker run alpine cal 
 1648  docker ps -a
 1649  docker ps
 1650  docker pull busybox
 1651  docker images
 1652  sleep 2
 1653  docker run alpine sleep 30
 1654  history 
 1655  docker run -d alpine sleep 30
 1656  docker ps
 1657  docker ps -a
 1658  docker ps
 1659  docker run -it alpine bash
 1660  docker run -it alpine sh
 1661  docker ps
 1662  exit
 1663  docker run -it alpine sh
 1664  docker ps
 1665  docker exec -it hopeful_liskov sh
```
```
sudo apt update ; sudo apt install docker.io
    2  docker ps
    3  sudo usermod -aG docker ubuntu
    4  docker ps
    5  sleep 10
    6  docker run -d myimg apache2ctl start
    7  docker ps
    8  docker ps -a
    9  docker run -it --name test myimg 
   10  docker commit 8f myserver
   11  docker images
   12  docker run -itd -p 1177:80 myserver 
   13  docker ps
   14  docker login
   15  docker images
   16  docker tag myserver aakashgaur57/myserver
   17  docker images 
   18  docker push aakashgaur57/myserver
   19  docker run -itd -p 7777:80 httpd
   20  docker ps
   21  vim index.html
   22  ls
   23  docker cp index.html happy_wozniak:/var/www/html/index.html
   24  sudo apt install mysql-server
   25  docker run --name phpmyadmin -d -e PMA_HOST=172.31.32.244 -p 8080:80 phpmyadmin
   26  docker ps
   27  ls -l /var/run/docker.sock 
   28  sudo vim /var/run/docker.sock 
   29  sudo cat  /var/run/docker.sock 
```
### docker network
```
docker network create net1 --subnet 192.168.0.0/16 
  223  docker network ls
  224  docker network inspect net1
  225  docker network create  net2 
  226  docker network ls
  227  docker network inspect net2
  228  docker run -itd --network net1 --name can1 alpine 
  229  docker ps
  230  docker rm -f laughing_feynman 
  231  docker ps
  232  docker inspect can1 | grep IPA
  233  docker run -itd --network net2 --name can3 alpine
  234  docker ps
  235  docker inspect can3  | grep IPA
  236  docker run -itd --network net1 --name can5 alpine
  237  docker run -itd --network net1 --name can2 alpine
  238  docker run -itd --network net2 --name can4 alpine
  239  docker run -itd --network net2 --name can6 alpine
  240  docker ps
  241  docker exec -it can1 sh 
  242  docker run -itd --network none apline
  243  docker run -itd --network none alpine
  244  docker ps
  245  docker inspect eager_ganguly | grep IPA
  246  docker run -itd --network host --name host alpine
  247  docker ps
  248  docker inspect host | grep IPA
  249  docker exec -it host sh
  250  ip a
  251  docker exec -it can1 sh
  252  docker network connect net2 can1
  253  docker exec -it can1  sh
```

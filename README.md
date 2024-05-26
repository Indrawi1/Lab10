# Lab10
docker network create --driver=bridge --subnet=11.0.11.0/24 lab10net
Tworzenie sieci
![image](https://github.com/Indrawi1/Lab10/assets/98088474/3bf54e07-e782-44e2-8d0a-abc7c5870814)
docker run -d --name web1 --network lab10net -p 8081:80 -v C:\Users\milen\lab10\web1\html:/usr/share/nginx/html:ro -v C:\Users\milen\lab10\web1\logs:/var/log/nginx nginx:latest
Tworzenie serwera web1 na porcie 8081
![image](https://github.com/Indrawi1/Lab10/assets/98088474/c66ff7c8-d36d-41b5-ae54-259e269c4118)
docker run -d --name web2 --network lab10net -p 8082:80 --volumes-from web1:ro -v ~/lab10/logs/web2:/var/log/nginx nginx:latest
docker run -d --name web3 --network lab10net -p 8083:80 --volumes-from web1:ro -v ~/lab10/logs/web2:/var/log/nginx nginx:latest
![image](https://github.com/Indrawi1/Lab10/assets/98088474/765c28cf-e98b-4dc8-9e53-a0e33c3e19de)
działanie serwerów
![image](https://github.com/Indrawi1/Lab10/assets/98088474/562bd0d7-9f36-48c8-986e-0a9a820488b3)
![image](https://github.com/Indrawi1/Lab10/assets/98088474/2deb302c-920f-428d-9277-2f50b9099625)
![image](https://github.com/Indrawi1/Lab10/assets/98088474/f0f6ccd5-1227-40d2-a350-fa5536858c0d)
![image](https://github.com/Indrawi1/Lab10/assets/98088474/6aff53f2-9458-46b5-81db-ff032e8d5239)
logi

![image](https://github.com/Indrawi1/Lab10/assets/98088474/7ece548f-1fb8-4984-a2a7-73fb619efe9a)







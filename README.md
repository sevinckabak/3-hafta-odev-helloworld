
# Pia Tech 3. Hafta Ödev

**Ödev:** Basit Bir Web Uygulaması için Docker ve Kubernetes Kullanarak Dağıtım Yapmak

**Amaç:** Bu ödev, Docker ve Kubernetes kullanarak bir web uygulamasını konteynerize etmeyi ve Kubernetes üzerinde dağıtmayı amaçlar. Ödevde Dockerfile oluşturma, Docker Hub’a görüntü yükleme, Kubernetes Deployment ve Service dosyalarını oluşturma ve uygulamanın Kubernetes üzerinde çalıştığını doğrulama adımları yer alır.

**Image oluşturma:** ```docker build -t helloworld.v1 .```

**Image kontrol:** ``docker images``

![image](https://github.com/user-attachments/assets/139c8e60-1b5b-4fdc-9490-478dc9eb586d)


Deployment ve servis dosyalarının bulunduğu dizine gidelim; ``cd k8s``

**Deployment dosyasını oluşturma:** 
``kubectl apply -f deployment.yaml``

**Servis dosyası oluşturma:**
``kubectl apply -f service.yaml``

**Deployment kontrol:** ``kubectl get deployment``

![image](https://github.com/user-attachments/assets/95dc336d-7703-44d6-a889-3bb0f5cd7638)

Helloworld-deployment 3 replikalı olarak oluşturuldu.

**Servis kontrol:**  ``kubectl get svc helloworld``

![image](https://github.com/user-attachments/assets/da0f9cd2-58e9-4c7c-b087-9389e4c3f85b)


Helloworld localhost 80 portunda çalışmaktadır.

![image](https://github.com/user-attachments/assets/e54cf102-8b86-4c92-a03f-98a55634af4e)


**Servis üzerinden poda bağlanarak çalışıp çalışmadığını kontrol edelim:** ``curl http://localhost:80``

![image](https://github.com/user-attachments/assets/d77a77c5-d4b8-4e5e-9555-b2927293734a)


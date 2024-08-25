
# Pia Tech 3. Hafta Ödev

Ödev: Basit Bir Web Uygulaması için Docker ve Kubernetes Kullanarak Dağıtım Yapmak

Amaç: Bu ödev, Docker ve Kubernetes kullanarak bir web uygulamasını konteynerize etmeyi ve Kubernetes üzerinde dağıtmayı amaçlar. Ödevde Dockerfile oluşturma, Docker Hub’a görüntü yükleme, Kubernetes Deployment ve Service dosyalarını oluşturma ve uygulamanın Kubernetes üzerinde çalıştığını doğrulama adımları yer alır.

Image oluşturma: docker build -t helloworld.v1 .
Image kontrol: docker images


Deployment dosyasını oluşturma:  cd k8s
kubectl apply -f deployment.yaml

Servis dosyası oluşturma:
kubectl apply -f service.yaml

Deployment kontrol: kubectl get deployment

Helloworld-deployment 3 replikalı olarak oluşturuldu.

Servis kontrol:  kubectl get svc helloworld



Helloworld localhost 80 portunda çalışmaktadır.

Servis üzerinden poda bağlanarak çalışıp çalışmadığını kontrol edelim: curl http://localhost:80

![image](https://github.com/user-attachments/assets/899d461f-e094-4e22-885c-04d207e33b54)

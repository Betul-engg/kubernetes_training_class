# Kubectl get pods

`kubectl get pods` komutu, Kubernetes kümesindeki pod'ları listelemek için kullanılır. Pod, Kubernetes'te en temel dağıtım birimidir ve bir veya daha fazla konteyneri içerebilir. İşte bu komutun detayları:

### Komutun Temel Kullanımı

```bash
kubectl get pods
```

Bu komut, mevcut namespace'deki (varsayılan olarak `default` namespace) tüm pod'ların listesini gösterir.

### Çıktı Alanları

Komut çalıştırıldığında tipik olarak aşağıdaki bilgileri içeren bir çıktı alırsın:

- **NAME**: Pod'un adı.
- **READY**: Pod'un içinde çalışan konteynerlerin sayısı (örneğin, `1/1` ifadesi, 1 konteynerin olduğunu ve bunun da çalıştığını gösterir).
- **STATUS**: Pod'un mevcut durumu (örneğin, `Running`, `Pending`, `Succeeded`, `Failed`, `CrashLoopBackOff` gibi).
- **RESTARTS**: Pod'un içinde çalışan konteynerlerin yeniden başlatılma sayısı.
- **AGE**: Pod'un oluşturulma süresini belirtir.

### Ek Seçenekler

- **Belirli bir Namespace'deki Pod'lar**: Eğer belirli bir namespace'deki pod'ları görmek istiyorsan:

  ```bash
  kubectl get pods -n <namespace-adı>
  ```

- **Detaylı Bilgi**: Daha fazla bilgi almak için `-o wide` seçeneğini kullanabilirsin:

  ```bash
  kubectl get pods -o wide
  ```

  Bu, pod'ların IP adreslerini ve hangi node üzerinde çalıştıklarını gösterir.

- **Belirli Bir Pod**: Tek bir pod hakkında daha fazla bilgi almak için:

  ```bash
  kubectl get pod <pod-adı>
  ```

- **Filtreleme**: Pod'ları belirli etiketlere göre filtrelemek için `-l` seçeneğini kullanabilirsin:

  ```bash
  kubectl get pods -l <etiket-adı>=<etiket-değeri>
  ```

### Örnekler

- Tüm pod'ları listelemek:

  ```bash
  kubectl get pods
  ```

- Belirli bir namespace'deki pod'ları listelemek:

  ```bash
  kubectl get pods -n my-namespace
  ```

- Detaylı bilgi ile pod'ları listelemek:

  ```bash
  kubectl get pods -o wide
  ```


------------------

kubectl describe pod <pod_name>

------------------

kubectl logs <pod_name>

---------------

kubectl exec -it <pod_name> -- /bin/bash

--------------

kubectl port-forward <pod_name> <local_port>:<pod_port>

-------------
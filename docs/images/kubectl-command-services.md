`kubectl` ile Kubernetes servislerini (services) yönetmek için kullanabileceğin temel komutlar şunlardır:

### 1. Tüm Servisleri Listeleme

```bash
kubectl get services
```

Bu komut, mevcut namespace'deki (varsayılan olarak `default`) tüm servisleri listeler.

### 2. Belirli Bir Namespace'deki Servisleri Listeleme

```bash
kubectl get services -n <namespace-adı>
```

Bu komut, belirtilen namespace içindeki servisleri gösterir.

### 3. Detaylı Bilgi ile Servisleri Listeleme

```bash
kubectl get services -o wide
```

Bu komut, servisler hakkında daha fazla bilgi (örneğin, IP adresleri ve portlar) sağlar.

### 4. Belirli Bir Servis Hakkında Bilgi Alma

```bash
kubectl get service <servis-adı>
```

Bu komut, belirli bir servis hakkında detaylı bilgi verir.

### 5. Servis Oluşturma

Yeni bir servis oluşturmak için bir YAML dosyası kullanabilirsin. Örneğin:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: my-app
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080
  type: ClusterIP
```

Bu dosyayı `my-service.yaml` adıyla kaydettikten sonra aşağıdaki komutla oluşturabilirsin:

```bash
kubectl apply -f my-service.yaml
```

### 6. Servisi Silme

```bash
kubectl delete service <servis-adı>
```

Bu komut, belirtilen servisi siler.

### 7. Servis Güncelleme

Bir servisi güncellemek için, öncelikle servisin mevcut tanımını almak ve ardından güncelleme yapmak istersen YAML dosyası üzerinde değişiklik yapabilirsin:

```bash
kubectl get service <servis-adı> -o yaml > my-service.yaml
```

Ardından dosyada değişiklik yapıp tekrar uygulayabilirsin:

```bash
kubectl apply -f my-service.yaml
```

### 8. Servis için Detaylı Bilgi Alma

```bash
kubectl describe service <servis-adı>
```

Bu komut, belirli bir servis hakkında ayrıntılı bilgi verir.

### 9. Etiketlere Göre Servisleri Filtreleme

Belirli etiketlere sahip servisleri listelemek için:

```bash
kubectl get services -l <etiket-adı>=<etiket-değeri>
```

Bu komut, yalnızca belirtilen etikete sahip servisleri gösterir.

Bu komutlar, Kubernetes servislerini yönetirken oldukça faydalıdır. Başka bir konuda yardımcı olmamı ister misin?
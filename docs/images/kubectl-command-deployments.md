`kubectl get deployments` komutu, Kubernetes kümenizdeki tüm dağıtımları (deployments) listelemek için kullanılır. İşte komutun nasıl kullanılacağına dair örnekler:

1. Tüm dağıtımları listelemek için:
   ```bash
   kubectl get deployments
   ```

2. Belirli bir ad alanındaki (namespace) dağıtımları listelemek için:
   ```bash
   kubectl get deployments -n <namespace-adı>
   ```

3. Daha fazla detay ile listelemek için:
   ```bash
   kubectl get deployments -o wide
   ```

4. Çıktıyı YAML formatında almak için:
   ```bash
   kubectl get deployments -o yaml
   ```

5. Çıktıyı JSON formatında almak için:
   ```bash
   kubectl get deployments -o json
   ```

Bu komutlar, Kubernetes dağıtımlarını yönetirken faydalı olacaktır. Başka bir şey sormak istersen, buradayım!
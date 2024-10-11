`kubectl get namespaces` komutu, Kubernetes kümenizdeki tüm ad alanlarını (namespaces) listelemek için kullanılır. İşte bu komutun nasıl kullanılacağına dair örnekler:

1. Tüm ad alanlarını listelemek için:
   ```bash
   kubectl get namespaces
   ```

2. Ad alanları hakkında daha fazla detay ile listelemek için:
   ```bash
   kubectl get namespaces -o wide
   ```

3. Çıktıyı YAML formatında almak için:
   ```bash
   kubectl get namespaces -o yaml
   ```

4. Çıktıyı JSON formatında almak için:
   ```bash
   kubectl get namespaces -o json
   ```


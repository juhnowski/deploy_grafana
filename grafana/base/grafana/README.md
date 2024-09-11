# Grafana
## Подготовка и установка
### Создание namespace
```bash
kubectl create namespace grafana
```

### Создание секретов

#### Grafana

```bash
export NAMESPACE=grafana

kubectl create secret generic -n "$NAMESPACE" grafana \
    --from-literal=GF_SECURITY_ADMIN_PASSWORD='root' \
    --from-literal=GF_SECURITY_ADMIN_USER='root'
```

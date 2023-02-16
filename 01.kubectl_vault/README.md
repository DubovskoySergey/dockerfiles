Образ написан для использования в gitlab ci, для получения секретов из хранилища vault и подлючения к кластеру k8s.

Образ основан на Alpine 3.17, в него установлены:
vault client v1.11.4;
kubectl v4.5.7.

Собранный образ можно скачать из Docker Hub
https://hub.docker.com/r/dubovskoy/kubectl_vault
Команда для скачавания
docker pull dubovskoy/kubectl_vault
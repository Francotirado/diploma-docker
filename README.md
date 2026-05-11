# Дипломный практикум в Yandex.Cloud

Данный репозиторий содержит файлы тестового приложения:

```
./
├── Dockerfile
├── main.py
├── README.md
└── requirements.txt
```

Для корректной отработки пайплайна необходимо наличие следующих секретов:

| Секрет | Значение секрета |
| --- | --- |
| YC_SA_KEY | Содержит ключ сервисного аккаунта создаваемого автоматически при создании сервисного аккаунта через Terraform для работы с Yandex Cloud |
| DIPLOMA_K8S_PAT | Содержит Personal Access Token Github'а для передачи триггера в репозиторий **diploma-k8s** | 

После отправки коммита в репозиторий, происходит сборка Docker образа и производится push в Registry и автоматически запускается триггер на активацию деплоя Kubernetes кластера в проекте `https://github.com/Francotirado/diploma-k8s.git`

Отработанный пайплайн билда и пуша Docker образа в Registry с демонстрацией его содержимого: 

![Ответ на задание 1](https://github.com/Francotirado/diploma-docker/blob/main/img/1.jpg)

![Ответ на задание 1](https://github.com/Francotirado/diploma-docker/blob/main/img/2.jpg)


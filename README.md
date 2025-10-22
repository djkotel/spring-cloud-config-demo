# Spring Cloud Config Demo

В этом архиве находятся три части:
- `config-repo` — локальный репозиторий конфигураций (yaml файлы)
- `config-server` — Spring Cloud Config Server
- `config-client` — Spring Boot клиент, который получает конфигурацию с Config Server

Как проверить:
1. В IntelliJ откройте проект `config-server` и `config-client` как отдельные maven modules (или import each separately).
2. Запустите Config Server (ConfigServerApplication). По умолчанию он ищет конфигурации в `../config-repo` относительного каталога `config-server`.
3. Проверьте в браузере: `http://localhost:8888/config-client/dev` — должен вернуться YAML с `message: "Привет из DEV окружения!"`
4. Запустите Config Client (ConfigClientApplication).
5. Перейдите: `http://localhost:8080/message` — увидите сообщение из профиля `dev`.

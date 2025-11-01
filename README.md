# Домашнее задание: Система мониторинга Zabbix
**Автор:** Константин Морозов

---

## Задание 1. Установка Zabbix Server с веб-интерфейсом

### Использованные команды:
```bash
sudo apt update
sudo apt install postgresql
sudo -u postgres createuser zabbix
sudo -u postgres createdb -O zabbix zabbix
sudo apt install zabbix-server-pgsql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent

```

### Скриншот авторизации в Zabbix

![Авторизация](screenshots/zabbix_login.png)

## Задание 2. Подключение Zabbix Agent и проверка работы

### Использованные команды

```bash
# Установка и запуск агента
sudo apt update
sudo apt install zabbix-agent -y
sudo systemctl enable zabbix-agent
sudo systemctl start zabbix-agent

# Проверка статуса агента
sudo systemctl status zabbix-agent

# Редактирование конфигурации
sudo nano /etc/zabbix/zabbix_agentd.conf

# Перезапуск после изменений
sudo systemctl restart zabbix-agent

# Проверка подключения с сервера
zabbix_get -s 127.0.0.1  -k agent.ping
>>>>>>> 77f574e (Добавлены скриншоты и команды для заданий)






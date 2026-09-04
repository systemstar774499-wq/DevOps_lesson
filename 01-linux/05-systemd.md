[boot]
systemd=true

# systemd

systemd — система инициализации и управления
службами Linux.

В моей Ubuntu systemd включён.

Проверка:

systemctl

Примеры:

systemctl status
systemctl start
systemctl stop
systemctl restart
systemctl enable

Просмотр журналов:

journalctl

## Почему важно для DevOps

Многие серверные приложения работают как службы.

Например:

Docker
GitLab Runner
SSH
Nginx

systemd позволяет управлять этими службами.
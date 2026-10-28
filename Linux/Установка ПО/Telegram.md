## Шаг 1. Подключаем Backports

Выполниит команду:

```bash
sudo tee /etc/apt/sources.list.d/debian-backports.sources > /dev/null <<'EOF'
Types: deb
URIs: https://deb.debian.org/debian
Suites: trixie-backports
Components: main
Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg
EOF
```

## Шаг 2. Обновляем список пакетов

```bash
sudo apt update
```

После этого проверяем Telegram:

```bash
apt policy telegram-desktop
```

## Шаг 3. Устанавливаем Telegram

```bash
sudo apt install -t trixie-backports telegram-desktop
```
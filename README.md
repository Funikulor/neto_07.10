# Настройка SSH-доступа к GitHub (Windows 10)

## 1. SSH-клиент и генерация ключей

- Проверка: `ssh -V` → OpenSSH_for_Windows_9.x ![Проверка](screenshots/check.png)
- Генерация: `ssh-keygen -t ed25519 -C "email"` ![Генерация](screenshots/generation.png)
- Passphrase установлена (подтверждение: ssh-keygen -y запрашивает пароль)
  ![Версия SSH](screenshots/ssh-version.png)

## 2. Публичный ключ добавлен в GitHub

![Ключ в настройках GitHub](screenshots/github-key.png)
![Добавление в ssh-agent](screenshots/ssh-agent.png)

## 3. Проверка подключения

`ssh -T git@github.com` → Hi USERNAME! You've successfully authenticated...
![Приветствие GitHub](screenshots/ssh-test.png)

## 4. Работа с репозиторием по SSH

git clone / commit / push — выполнены без ввода пароля
![Push](screenshots/git-push.png)

# Создание ssh ключа
1. В терминале эта команда со своей почтой для Git, passphrase скипаем Enter
```console
foo@bar:~$ ssh-keygen -t ed25519 -C "email@example.com"
```
Создадутся два ключа: ex и ex.pub
2. Добавление ключа
```console
foo@bar:~$ eval "$(ssh-agent -s)"
foo@bar:~$ ssh-add ex
```
# Добавление публичного ключа в Git
1. Копируем содержимое ex.pub
2. GitHub -> Profile Settings -> SSH and GPG keys -> New SSH key
3. В поле "Key" вставляем публичный ключ
4. Add SSH key
# Клонирование репозитория через SSH
1. В GitHub репозиторие скопировать SSH ссылку
2. Клонирование
```console
foo@bar:~$ git clone "git@github.com:username/repo.git"
```


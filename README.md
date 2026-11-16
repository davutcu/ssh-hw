
1. Проверили наличие SSH-клиента: ssh -V.
2. Сгенерировали новую пару ключей: ssh-keygen -t ed25519 -C "ismallova.xennia@gmail.com"` (screenshots/keygen.png).
3. Защитили приватный ключ паролем (passphrase).
4. Публичный ключ сохранён в ~/.ssh/: /c/Users/Huawei/.ssh/id_ed25519.pub 
5. Запустили агента: eval $(ssh-agent -s)
6. Добавили ключ в агента: ssh-add ~/.ssh/id_ed25519.
7. Скопировали публичный ключ в буфер обмена (clip < ~/.ssh/id_ed25519.pub): ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIKHI85hlZ3azUW73Ij/XjgagTYxH8ft6RrYfia53sLZS ismallova.xennia@gmail.com
8. Открыли GitHub: Settings → SSH and GPG keys → New SSH key [github-key](screenshots/github-key)
9. Добавили ключ в список, подтвердили добавление.
10. Запустили в терминале: ssh -T git@github.com.
11. При первом подключении подтвердили доверие хосту (yes), GitHub добавлен в known_hosts.
12. Получили приветствие: «Hi davutcu! You've successfully authenticated, but GitHub does not provide shell access
13. Создали на GitHub новый репозиторий: ssh-hw.
14. Склонировали репозиторий по SSH-URL: git clone git@github.com:davutcu/ssh-hw.git
15. Отредактировали README.md, выполнили git add, git commit -m Add README with screenshots 
16. Ссылка на репозиторий: https://github.com/davutcu/ssh-hw
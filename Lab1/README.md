
## Лабораторна робота №1


**Ціль роботи: Навчитися створювати репозиторії на GitHub, працювати з ssh ключами, оформляти профіль.**

Хід роботи:

# 1) Створив обліковий запис GitHub:

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.001.png)

Рисунок 1 – Профіль на GitHub

Посилання: <https://github.com/AlexAnastasiev>

# 2) Встановив Chocolatey:

Запустив *powershell* від імені адміністратора та виконав команду

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.002.png)

Рисунок 2 – Windows PowerShell

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

# 3) Встановив *git* на комп'ютер за допомогою Chocolatey:

Командою choco install git -y

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.003.png)

Рисунок 3 – Встановлений Git 

# 4) Налаштував *git*:

git config --global user.name "Alex Anastasiev"

git config --global user.email ananasss1999@gmail.com

# 5) Створив новий SSH ключ:

ssh-keygen -t ed25519 -C " ananasss1999@gmail.com "

# 6) Додав ключ до облікового запису Github:

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.004.png)

Рисунок 4 – Доданий SSH ключ до GitHub

# 7) Виставив потрібні налаштування і створив новий репозиторій в GitHub

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.005.png)

Рисунок 5 – Новий репозиторій в GitHub

# 8) Забрав копію на локальний ПК

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.006.png)

Рисунок 6 – Копіювання посилання

Для клонування репозиторію використав команду:

git clone git@github.com:AlexAnastasiev/AlexAnastasiev.git

# 9) Налаштував опис свого профілю

![](Aspose.Words.6ad609b3-a67e-4374-866c-f8d4bc7471c2.007.png)

Рисунок 6 – Опис головної сторінки профілю

# 10) Завантажив файли за допомогою команд:

git add .

git commit -m "Коментар"

git push


# ВИСНОВОК

В данній лабораторній роботі було виконано дії по роботі з Git, а саме:

1) Створили обліковий запис у GitHub;
2) Встановили Chocolatey та Git, налаштували його (також встановили ConEmu);
3) Згенерували ключ SSH, та створили репозиторій. Скопіювали його на ПК. Відредагували профіль і завантижили його на GitHub.


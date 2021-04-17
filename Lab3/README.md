
**Лабораторна робота №3**


## Мета роботи: Створити віртуальну машину з ОС Debian GNU/Linux. Створити  VPC мережу. Розгорнути інструмент для безперервної інтеграції, доставки та розгортання коду.

Хід роботи:

# 1) Створив VPC: GPC > Navigation menu > VPC network > Create vpc network.

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.001.png)

Рисунок 1 – Новостворена VPC

Одразу змінив налаштування фаерволу: ввімкнув тригер “tcp”, та додав порт :8080. 

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.002.png)

Рисунок 2 – Додавання порту



# 2) Cтворив нову віртуальну машину с ОС Debian GNU/Linux 10. 

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.003.png)

Рисунок 3 – Створення нової віртуальної машини

# 3) Обрав потрібні налаштування та сервісний обліковий запис. 


![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.004.png)

Рисунок 4 – Налаштування VM



# 4) Вибрали створену VPC мережу.

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.005.png)

Рисунок 5 – Налаштування мережі для VM 


# 5) Запустив VM: Navigation menu > Compute Engine > VM instance > “SSH”.

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.006.png)

Рисунок 6 – Відкрита VM у вікні браузера



# 6) Розгорнув інструмент для безперервної інтеграції, доставки та розгортання коду.

Виконав команди :

~$ sudo apt install – встановка пакету;

~$ sudo apt update – оновлення репозиторію;

~$ sudo apt search openjdk – пошук доступних версій Java;

~$ sudo apt install openjdk-11-jdk – встановлення вибраної версії;

~$ sudo apt update ;

~$ java -version ;

~$ sudo apt install wget – встановлення менеджеру завантажень;

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.007.png)

Рисунок 7 – Перевірка версії Java

Додав ключ репозиторію в систему та адресу репозиторію пакетів Debian в source.list серверу:

~$ wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add - 

~$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' 

~$ sudo apt update 

# 7) Встановив Jenkins:

~$ sudo apt install jenkins

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.008.png)

Рисунок 8 – Встановлення Jenkins

# 8) Запустив Jenkins та перевірив статус:

~$ sudo systemctl start jenkins 

~$ sudo systemctl status jenkins 

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.009.png)

Рисунок 9 – Запуск Jenkins

Щоб налаштувати установку, відкрив Jenkins на використовуваному за замовчуванням порті 8080, використовуючи о IP-адресу:

` `<http://34.66.28.246:8080/>. 

# 9) Ввів команду для виведення паролю: 

~$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.010.png)

Рисунок 10 – Згенерований пароль

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.011.png)

Рисунок 11 – Вікно розблокування

# 10) Для налаштування Jenkins потрібно встановити плагіни. Вибрав Install suggested plugins (рекомендовані).

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.012.png)

Рисунок 12 – Вибір методу встановлення плагінів


![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.013.png)

Рисунок 13 – Встановлення плагінів

# 11) Створив обліковий запис адміністратора.

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.014.png)

Рисунок 14 – Створення облікового запису



# 12) Натиснув Start using Jenkins (почати використання Jenkins), щоб відкрити панель управління Jenkins.

![](Aspose.Words.14a0d664-00c9-41ab-8e6e-bedcb2bfeae4.015.png)

Рисунок 15 – Панель Jenkins 

# 13) Додав звіт з виконаної лабораторної роботи на GitHub:

<https://github.com/AlexAnastasiev?tab=repositories>

## ВИСНОВОК

В данній лабораторній роботі було виконано дії по створенню віртуальної машини, на ОС Debian GNU/Linux 10  у GСP. Створено VPC; Налаштовано VM та мережу; Розгорнуто інструмент для безперервної інтеграції, доставки та розгортання коду. Встановлено Jenkins за допомогою пакетів, запущено сервер, і створено користувача з правами адміністратора. 


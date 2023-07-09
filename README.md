Итоговая контрольная работа по блоку специализация
pictures for project

Урок 2. Итоговая контрольная работа
https://github.com/Omegaiiii/-/edit/main/README.md#L<65>

Информация о проекте

Необходимо организовать систему учета для питомника в котором живут домашние и вьючные животные.
Как сдавать проект

Для сдачи проекта необходимо создать отдельный общедоступный репозиторий (Github, Gitlub или Bitbucket). Разработку вести в этом репозитории, использовать пул реквесты на изменения. Программа должна запускаться и работать, ошибок при выполнении программы быть не должно. Программа может использоваться в различных системах, поэтому необходимо разработать класс в виде конструктора.

Задание
Используя команду cat в терминале операционной системы Linux, создать два файла "Домашние животные" (заполнив файл "собаками", "кошками", "хомяками") и "Вьючные животные" (заполнив файл "лошадьми", "верблюдами" и " ослами"), а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя "Друзья человека".

Создать директорию, переместить файл туда.

Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.

Установить и удалить deb-пакет с помощью dpkg.

Выложить историю команд в терминале Ubuntu.

Нарисовать диаграмму, в которой есть классы - родительский, домашние животные и вьючные животные, в составы которых в случае домашних животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные войдут: лошади, верблюды и ослы.

В подключенном MySQL репозитории создать базу данных “Друзья человека”.

Создать таблицы с иерархией из диаграммы в БД.

Заполнить низкоуровневые таблицы именами (животных), командами которые они выполняют и датами рождения.

Удалить из таблицы верблюдов, т.к. верблюдов решили перевезти в другой питомник на зимовку. Объединить таблицы "лошади", и "ослы" в одну таблицу.

Создать новую таблицу "молодые животные" в которую попадут все животные старше 1 года, но младше 3 лет и в отдельном столбце, с точностью до месяца, подсчитать возраст животных в новой таблице.

Объединить все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам.

Создать класс с Инкапсуляцией методов и наследованием по диаграмме.

Написать программу, имитирующую работу реестра домашних животных. В программе должен быть реализован следующий функционал:

14.1. Завести новое животное;

14.2. Определять животное в правильный класс;

14.3. Увидеть список команд, которое выполняет животное;

14.4. Обучить животное новым командам;

14.5. Реализовать навигацию по меню.

Создайте класс Счетчик, у которого есть метод add(), увеличивающий̆ значение внутренней̆ int переменной̆ на 1 при нажатии “Завести новое животное”. Сделайте так, чтобы с объектом такого типа можно было работать в блоке try-with-resources. Нужно бросить исключение, если работа с объектом типа счетчик была не в ресурсном try и/или ресурс остался открыт. Значение считать в ресурсе try, если при заведения животного заполнены все поля.

Решение
1.
<details>
<summary>Команды Bash</summary>

cat > "Домашние животные"

Собаки

Кошки

Хомяки

'Ctrl+d'

</details>
<details>
<summary>Команды Bash</summary>

cat > "Вьючные животные"


Лошади

Верблюды

Ослы

'Ctrl+d'

</details>
<details>
<summary>Команды Bash</summary>

cat "Домашние животные" "Вьючные животные" > Animals


cat Animals

mv "Animals" "Друзья человека"

</details>

![1_2 (1)](https://github.com/Omegaiiii/-/assets/136469312/1087fde5-9bd5-4df8-8f9e-ba8ce245d589)

2.
<details>
<summary>Команды Bash</summary>

mkdir folder_for_attestation

mv 'Друзья человека' folder_for_attestation/

ls

cd folder_for_attestation/

ls

</details>

![2 (1)](https://github.com/Omegaiiii/-/assets/136469312/d998c475-315f-46e1-9c96-20e03c07e71e)
3.
<details>
<summary>Команды Bash</summary>

sudo apt-get update

sudo apt update

sudo apt install mysql-server

sudo service mysql status

</details>

![3_1 (1)](https://github.com/Omegaiiii/-/assets/136469312/e5d7e720-ef14-43e0-bcf8-5aeb035c9d52)
![3_2 (1)](https://github.com/Omegaiiii/-/assets/136469312/f7ab7450-b2bf-4e46-b994-3f1decadddb3)
![3_3 (1)](https://github.com/Omegaiiii/-/assets/136469312/2c8ef4f1-887f-4a6b-83bf-4fee168c85bb)
![3_4 (1)](https://github.com/Omegaiiii/-/assets/136469312/d083facb-79ef-45f3-b1a1-7885a7a4c069)
4.

<details>
<summary>Команды Bash</summary>

wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb

sudo dpkg -i sl_5.02-1_amd64.deb

sudo dpkg -r sl

</details>

![4_2 (1)](https://github.com/Omegaiiii/-/assets/136469312/9679e485-9200-4543-9cc5-07d572a219a0)

5.
<details>
<summary>Команды Bash</summary>

  730  mkdir attestation

  731  cd attestation/

  732  cat > Домашние животные

  733  cat > "Домашние животные"

  734  cat > "Вьючные животные"

  735  cat "Домашние животные" "Вьючные животные" > Animals 

  736  cat Animals

  737  mv "Animals" "Друзья человека"

  738  clear

  739  mkdir folder_for_attestation && mv "Друзья человека" /attestation/folder_for_attestation 

  740  ls

  741  rmdir folder_for_attestation/

  742  ls

  743  clear

  744  mkdir folder_for_attestation

  745  mv "Друзья человека" /attestation/folder_for_attestation

  746  mv "Друзья человека" attestation/folder_for_attestation

  747  ls

  748  mkdir folder_for_attestation

  749  rmdir folder_for_attestation

  750  clear

  751  mkdir folder_for_attestation

  752  mv 'Друзья человека' attestation/folder_for_attestation/

  753  mv 'Друзья человека' folder_for_attestation/

  754  ls

  755  cd folder_for_attestation/

  756  ls

  757  clear

  758  cd..

  759  cd.

  760  cd..

  761  cd 

  762  cd attestation/

  763  clear

  764  sudo apt-get update

  765  sudo apt update

  766  sudo apt install mysql

  767  sudo apt install mysql-server

  768  sudo service mysql status

  769  clear

  770  wget http://ftp.us.debian.org/debian/pool/main/s/sl/sl_5.02-1_amd64.deb

  771  sudo dpkg -i sl_5.02-1_amd64.deb

  772  sudo dpkg -r sl

  773  clear

  774  history


</details>

![5 (1)](https://github.com/Omegaiiii/-/assets/136469312/8863cd53-631a-4460-ae9d-1bad4c9e2b29)
6.
![diagram (1)](https://github.com/Omegaiiii/-/assets/136469312/a601f894-8945-4723-98f4-b32167d7ea0a)
7.
CREATE DATABASE Друзья_человека;
![7 (1)](https://github.com/Omegaiiii/-/assets/136469312/a5769b83-6f93-455b-8fb9-523b31a65ed2)
8.
<details>
<summary>Команды Bash</summary>

CREATE TABLE Родительский_класс (

  id INT PRIMARY KEY AUTO_INCREMENT,
  
  тип VARCHAR(50)
);


CREATE TABLE Домашние_животные (

  id INT PRIMARY KEY,
  
  вид VARCHAR(50),
  
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
  
);


CREATE TABLE Собаки (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,
  
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
  
);


CREATE TABLE Кошки (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,
  
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
  
);


CREATE TABLE Хомяки (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,
  
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
  
);


CREATE TABLE Вьючные_животные (

  id INT PRIMARY KEY,

  вид VARCHAR(50),
  
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
  
);


CREATE TABLE Лошади (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,
  
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
  
);


CREATE TABLE Верблюды (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,

  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
  
);


CREATE TABLE Ослы (

  id INT PRIMARY KEY,
  
  имя VARCHAR(50),
  
  команда VARCHAR(50),
  
  дата_рождения DATE,
  
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
  
);

show databases;

show tables;

</details>

![8 (1)](https://github.com/Omegaiiii/-/assets/136469312/a3841270-8208-4ad2-81df-2d03869f1fde)
9.
<details>
<summary>Команды Bash</summary>

INSERT INTO Верблюды ( имя, команда, дата_рождения)

VALUES ('Зефир', 'Но, пошел', '2019-09-01'),

       ('Багдад', 'На месте' '2020-11-12'),
       
       ('Скорость', 'Ждать' '2021-04-05');
       

INSERT INTO Кошки ( имя, команда, дата_рождения)

VALUES ('Маркиз', 'Кис-кис', '2021-01-20'),

       ('Снежка', 'Давай играть', '2022-03-08');
       

INSERT INTO Лошади ( имя, команда, дата_рождения)

VALUES ('Спирит', 'Но', '2020-01-21'),

       ('Воронок', 'Бррррр', '2022-03-08');
       

INSERT INTO Ослы ( имя, команда, дата_рождения)

VALUES ('Нарик', 'Пошёл', '2019-01-21'),

       ('Степан', 'Стой', '2021-03-08');
       

INSERT INTO Собаки ( имя, команда, дата_рождения)

VALUES ('Шарик', 'Дай лапу', '2019-01-21'),

       ('Бим', 'Лежать', '2020-03-08');

       

INSERT INTO Хомяки ( имя, команда, дата_рождения)

VALUES ('Долгожитель', 'Кушать', '2022-01-21'),

       ('Хома', 'Отойди', '2023-03-08');

       

</details>
10.
<details>
<summary>Команды Bash</summary>

TRUNCATE TABLE Верблюды;

</details>
<details>
<summary>Команды Bash</summary>

CREATE TABLE Парнокопытные AS

SELECT * FROM Лошади

UNION

SELECT * FROM Ослы;

</details>
11.
<details>
<summary>Команды Bash</summary>

CREATE TABLE Парнокопытные AS

SELECT *, TIMESTAMPDIFF(MONTH, дата_рождения, CURDATE()) AS возраст_в_месяцах

FROM (

    SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
    
    UNION ALL
    
    SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
    
    UNION ALL
    
    SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
    
    UNION ALL
    
    SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
    
    UNION ALL
    
    SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы
    
) AS животные

WHERE дата_рождения >= DATE_SUB(CURDATE(), INTERVAL 3 YEAR)

AND дата_рождения <= DATE_SUB(CURDATE(), INTERVAL 1 YEAR);


</details>
12.
<details>
<summary>Команды Bash</summary>

CREATE TABLE Полный_состав AS

SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки

UNION ALL

SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки

UNION ALL

SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки

UNION ALL

SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади

UNION ALL

SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы;



</details>
13.14.15 - код Java https://github.com/Omegaiiii/-/tree/main/Java
Подготовил студент Geek Brains Вербицкий Руслан, Final_control_work_on_the_specialization_block




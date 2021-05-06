# lab3
МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ

Національний аерокосмічний університет ім. М. Є. Жуковського «Харківський авіаційний інститут»

Факультет «Радіоелектроніки, комп’ютерних систем та інфокомунікацій» Кафедра «Аерокосмічних радіоелектронних систем»

Лабораторна робота №3

з дисципліни «Інформаційно-комунікаційні мережі »

на тему: «Створення віртуальної машини з операційною системою лінукс»

Виконав: студент 4 курсу групи № 536-ст напряму підготовки (спеціальності) 172 «Телекомунікації та радіотехніка» Лазурко В.Є.

Прийняв: ас. каф. 501

Перетятько М. С.

Національна шкала:

Кількість балів:

Оцінка: ECTS

Харків 2021

Ціль роботи: Створити віртуальну машину з операційною системою лінукс.

ХІД РОБОТИ

1. Cтворюємо новий проект у GCP
![image](https://user-images.githubusercontent.com/79759252/117306573-73695400-ae88-11eb-903a-76cd5af2e372.png)
2. Створив VPC
![image](https://user-images.githubusercontent.com/79759252/117307318-220d9480-ae89-11eb-81b1-a9234fe078ab.png)
3.Створюємо віртуальну машину з операційною системою лінукс
![image](https://user-images.githubusercontent.com/79759252/117307451-41a4bd00-ae89-11eb-8703-39be08e44968.png)
4. Виконуємо команди з сайта https://www.jenkins.io/doc/book/installing/linux/#debianubuntu

А саме:
Спочатку оновлюємо наш Дебиан

sudo apt-get update
sudo apt update

Встановлюємо Java
sudo apt install openjdk-11-jdk
sudo apt install wget

Виконуємо команди з сайту
![image](https://user-images.githubusercontent.com/79759252/117354047-9102e180-aeb9-11eb-94c3-bd99550d0a22.png)

Тепер перевіряємо роботу Jenkins
![image](https://user-images.githubusercontent.com/79759252/117354143-abd55600-aeb9-11eb-86b0-b32254183d01.png)

Переконались що Jenkins працює
Якщо не працює його можна запустити командою
sudo systemctl status jenkins

Переходимо на сторінку віртуальних машин і вибираємо наш зовнішній IP
![image](https://user-images.githubusercontent.com/79759252/117354401-f22ab500-aeb9-11eb-9132-816badb554d2.png)

Отримаємо непрацюючий сайт.
![image](https://user-images.githubusercontent.com/79759252/117354479-0c649300-aeba-11eb-8ed2-3409ed925a62.png)
Для вирішення проблеми спочатку потрібно вибрати не https:// , а http://
і в кінці дописати ":8080"
Якщо не працює то в VPC Network потрібно змінити 
![image](https://user-images.githubusercontent.com/79759252/117354726-5cdbf080-aeba-11eb-9301-ffea3a59988c.png)
його потрібно редагувати та дописати
![image](https://user-images.githubusercontent.com/79759252/117354854-8563ea80-aeba-11eb-8a58-d9b35cd9c0b7.png)
Заходимо на сторінку, тепер можемо бачити там поле для паролю та красну строчку шляху
В нашій віртуальній машині пишемо 
sudo cat <червона строчка>
Копіюємо пароль та вставляємо в поле
Проходимо реєстрацію
І все Jenkins готовий
![image](https://user-images.githubusercontent.com/79759252/117355268-08854080-aebb-11eb-801b-233f74da782e.png)
Висновок: В данній роботі навчились створювати віртуальну машину підключати її до мережі, відкривати порт 8080, та встановили на неї Jenkins. Зареєструвалися в ньому. Виникли труднощі з підключенням по зовнішньому IP, але відео зняте одногрупниками допомогло знайти помилку та не вступити в різні пастки. 

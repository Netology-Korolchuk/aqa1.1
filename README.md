# Домашнее задание к занятию «1.1. Основы автоматизации»

Не забывайте заводить по найденным багам баг-репорты в Github Issue.

В качестве результата пришлите ссылку на ваш GitHub-проект в личном кабинете студента на сайте [netology.ru](https://netology.ru).

Все задачи этого занятия нужно делать в одном репозитории.

**Важно**: не делайте ДЗ всех занятий в одном репозитории! Иначе вам потом придётся достаточно сложно подключать системы Continuous Integration.

## Как сдавать задачи

1. Инициализируйте на своём компьютере пустой Git-репозиторий
1. Добавьте в него готовый файл [.gitignore](../.gitignore)
1. Добавьте в этот же каталог код вашего приложения
1. Сделайте необходимые коммиты
1. Создайте публичный репозиторий на GitHub и свяжите свой локальный репозиторий с удалённым
1. Сделайте пуш (удостоверьтесь, что ваш код появился на GitHub)
1. Ссылку на ваш проект отправьте в личном кабинете на сайте [netology.ru](https://netology.ru)

В качестве примера можете посмотреть на этот проект (ваш по структуре должен выглядеть так же): https://github.com/netology-code/aqa-hw-sample


## Задача №1 - CashbackHacker

Вы участвуете в проекте CashbackHacker - небольшой сервис, который сообщает пользователю о том, сколько ему нужно "докупить" в рамках конкретной траты, чтобы получить максимальное количетство кэшбека.

Подробнее: кэшбек начисляется за каждую потраченную полную тысячу рублей, поэтому если вы покупаете что-то на 900 рублей, сервис должен посоветовать вам докупить "ещё чего-нибудь" на 100 рублей.

Код сервиса выглядит следующим образом:

```java
package ru.netology.service;

public class CashbackHackService {
    private final int boundary = 1000;

    public int remain(int amount) {
        return boundary - amount % boundary;
    }
}
```

Вам нужно создать проект на базе Gradle (как на лекции), добавить в него JUnit 5 (прописать их в `build.gradle`) и написать авто-тесты, которые тестируют функциональность этого сервиса (как минимум, два).

В сервисе точно есть ошибка, поэтому один из ваших авто-тестов должен падать.

Выложите полученный проект на GitHub. Не забудьте про файл [.gitignore](../.gitignore).

<details>
    <summary>Подсказка</summary>

    Если пользователь купил ровно на 1000 рублей, то приложение не должно ему говорить, что нужно купить ещё на 1000.
</details>

## Задача №2 - Репортинг (необязательная)

Создайте issue на GitHub (в рамках первого проекта), к которому приложите архив с отчётами Gradle.

Напоминаю, выглядеть они (отчёты) должны примерно вот так (у вас должно быть не 100% successful):

![](pic/report.png)

В личном кабинете вам нужно будет отправить ссылку на то issue, что вы создали (для демонстрационного проекта это: https://github.com/netology-code/aqa-hw-sample/issues/1)

# Инструкция по работе с Git

## Что такое Git?

Git - одна из реализаций распределённых систем контроля версий, имеющая как локальную версионность, так и версионность на сервере. Git является самой популярной системой контроля версий на сегодняшний день.

## Подготовка репозитория

Для того, чтобы создать репозиторий в указанной папке используется команда *git init*. Для этого достаточно написать команду *git init* в папке с будущим репозиторием.

## Создание "сохранений"

Для того, чтобы добавить файл к новому коммиту("сохранение") необходимо использовать команду *git add*. Используется она следующим образом: в папке с репозиторием пишем команду *git add <имя файла>*

## Создание фиксаций

Для создания новой фиксации необходимо использовать команду *git commit*. Используется она следующим образом: в папке с репозиторием пишется команда *git commit -m "<сообщение к коммиту>"*. Все файлы коммита должны быть предварительно добавлены с помощью команды *git add*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

### Просмотр информации об изменениях

Для того, чтобы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду *git status*. Для этого достатчно использовать *git status* в папке с репозиторием.

### Подготовка файла для коммита

Для просмотра изменений в файлах, которые ещё не были добавлены в индекс коммита, существует команда *git diff*. Она вводится в строку, и можно увидеть разницу между файлами. Еще эту команду называют дифференциация.

## Перемещение между сохранениями

Для перемещения между ветками существует команда *git checkout*. Чтобы перейти с одной ветки на другую необходимо ввести команду *git checkout <имя ветки>*

## Журнал изменений

За просмотр истории коммитов отвечает команда *git log*. Достаточно ввести эту команду в строку,и можно увидеть все команды от новых к старым, т.е. в обратном порядке. Для каждого коммита выводится 
* хеш
* автор
* дата
* сообщение(commit message)

## Ветки в Git

Используя ветвление, можно отклоняться от основной линии разработки и продолжать работу независимо от неё. Операция создания ветки выполняется легко и почти мгновенно, переключение между ветками также, обычно, быстро. Чтобы создать ветку, надо в строке написать команду *git branch <имя ветки>*. Существует несколько команд для работы с ветками:

* git branch - выводит список веток
* git branch -d <имя ветки> - удаляет слитую ветку
* git branch images - вставляет изображение в текст c помощью знака **! [ ] ( )**
 


## Слияние веток и разрешение конфликтов

### Слияние веток

Для слияния веток используется команда *git merge <имя ветки, которую нужно влить>*, и она сольётся с главной веткой, т.е. с той, в которой мы находимся в данный момент.

### Разрешение конфликтов

Когда в разных ветках один и тотже текст написан по-разному, при слиянии таких веток происходит **КОНФЛИКТ**. Самый простой способ разрешить конфликт - отредактировать конфликтующий файл, после чего необходимо выполнить команду *git add merge

## Удаление веток
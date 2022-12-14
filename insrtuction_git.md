# Инструкция по работе с Git

![привет, это Саша!](Sasha.JPG)

Git - это программа, которая отвечает за отслеживание и ведение истории изменения файлов, в вашем проекте. Чаще всего его используют для кода.
## Создание нового репозитория

Чтобы создать новый репозиторий (инициализировать) нужно ввести команду:

    git init
## Проверка актуального состояния репозитория

Для того, чтобы проверить в каком состоянии находится репозиторий нужно ввести команду:
    
    git status

## Создание commit
Для того, чтобы создать новый commit необходимо сначала указать файл, в котором этот commit будет сделан. Для этого используется команда:

    git add

Далее создаем сам commit с помощью команды:

    git commit
    либо сразу с подписью в той же строке:
    git commit -m "maessege"

Чтобы объединить два предыдущих пункта вместе используется команда:

    git commit -am "messege"

## Просмотр изменений
Чтобы увидеть изменения между текущей и последней закоммиченной версиями используется команда

    git diff

Для просмотра изменений между двумя закоммиченными версиями используется таже команда и имена двух коммитов, между которыми нужно посмотреть разницу:

    git diff <hash1> <hash2>

# Список всех commit
Чтобы посмотреть список всех созданных commit в документе, необходимо ввести следующую команду:

    git log
    либо 
    git log --all

Для выведения того же списка в более сжатом (коротком) виде используется:

    git log --oneline
    либо git log --oneline --all

Для выхода из режима просмотра сохраненных commit используется клавиша:

    q

Для возвращения в текущую версию файла:

    git checkout <brunch name>

## Проверка статуса документа в конце работы
После окончания работы с документом необходимо проверить его статус, чтобы убедиться в том, что все изменения сохранены.

    git status


## Ветвления
Ветвления в Git нужны для параллельного создания нескольких вариантов одного документа. Это необходимо, если над документом одновременно работает несколько человек.

### Отображение всех имеющихся веток
Для отображения всех веток используется команда:

    git branch
    
### Создание новой ветки    
Чтобы создать новую ветку используется команда

    git branch <branch_name>

### Переключение между ветками
Чтобы переключиться на другую ветку используется команда

    git checkout <branch_name>

### Структура ветвлений в репозитории
Чтобы посмотреть структуру ветвлений и слияний используется команда 

    git log --graph
    или для более компактного отображения структуры
    git log --graph --all --oneline

### Слияние двух веток, возникновение конфликтов
При слиянии двух веток используется команда

    git merge <branch_mame>

При этом, для осуществления слияния необходимо перейти на основную ветку, с которой будет происходить слияние
В случае возникновения конфликтов версий при слиянии, небходимо в ручном режиме отредактировать нужный вариант версий,  либо выбрать из вариантов, которые предложит программа.

### Удаление ненужной ветки

Для удаления ненужной ветви необходимо использовать команду:

    git branch -d <branch_mame>

## Удаленные репозитории

Удаленные репозитории нужны для ...

# Инструкция для работы с Git и удалёнными репозиториями
# Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
# Подготовка репозитория
Для создание репозитория необходимо выполнить команду _git init_ в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

# Создание коммитов
## Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду git add напишите *git add <имя файла>*

## Просмотр состояния репозитория
---
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

Для того, чтобы **ОДНОВРЕМЕННО** добавить изменения в коммит (*git add*) и создать коммит (*git commit*) необходимо выполнить команду: *git commit -am "<сообщение к коммиту>"*

Для того, чтобы увидеть разницу между текущим файлом и закоммиченным файлом необходимо выполнить команду *git diff*.

# Добавление картинок
## Картинка
   ![картинки](https://miro.medium.com/max/1400/1*vlDY5078rLn0dFQWbdAKUA.png)
## Гифка
   ![гиф](https://raw.githubusercontent.com/nadehi18/battery-wallpaper-windows/master/preview/charging.gif)
## Картинка из папки
   ![картинка](1_S-_fv45WT4MgqtnPVsxtHQ.jpeg)

# Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

Для того, чтобы вернуться к актуальному состоянию и продиолжить работу с файлом используется команда *git checkout master*.

# Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда _git log_. Для этого достаточно выполнить команду _git log_ в папке с репозиторием

Для того, чтобы посмотреть сделанные изменения (коммиты) по всем веткам репозитория ("дерево изменений"), используется команда *'git log --graph'*

# Ветки в Git
## Создание ветки
Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*
## Слияние веток
Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*
## Удаление веток
Для удаления ветки ввести команду "git branch -d 'name branch'"

# Игнорирование файлов
Как правило, в Git-программах принято работать только с текстом, а изображения, видео и другие крупные файлы хранят в других папках, файлах, хранилищах и т.д. 
Поэтому, после добавления в наш файл, к примеру, изображения - не надо его коммитить (сохранять). 

Однако, при этом Git постоянно будет напоминать вам и предлагать сохранить внесенные изменения.

Для таких случаев в текущем репозитории создаётся отдельный файл *'.gitignore'*. 

В данный файл необходимо добавить файлы, которые Git должен игнорировать.
При этом указываем либо полное название игнорируемых файлов *(<image.jpg>)*, либо расширение всех файлов, которые необходимо игнорировать с символами " * " и " . " перед типом расширения _(<*.png и т.д.)_.

После добавления файлов в папку *'.gitignore'* - их названия становяться серого цвета в директории *explorer*, а Git не будет указывать данные файлы незакоммиченными (хотя сами файлы будут сохранены в нашем основном редактируемом файле!).

Если на локальном устройстве установлена программа *'dot.net'*, то файл *'.gitignore'* можно создать через команду *'dotnet new gitinore'*.
## Several main git commands to work with VCS
* Создать config c двумя параметрами user_name и email:
```
    git config --global user.name "Kobe Bryant"
    git config --global user.email kobebryant@gmail.com
```
* Просмотреть все настройки конфигурации Git:
```
    git --list
```
* Задать редактор для записи commit:
```
    git config --global core.editor nano
```
* Создание нового Git репозитория:
```
    git init
```
* Просмотреть текущее состояние индекса (staging area):
```
    git status
```
* Просмотреть и сравнивнить содержимое рабочего каталога с содержимым индекса (staging area):
```
    git diff
```
* Просмотреть и сравнивнить содержимое любых двух commit:
```
    git diff <commit1 hash> <commit2 hash>
```
* Добавить script.js или все файлы в индекс (staging area) репозитория:
```
    git add script.js || git add . || git -a (--all)
```
* Добавить все файлы с расширением .js в индекс (staging area) репозитория:
```
    git add *.js
```
* Отменить изменения script.js внесенные в индекс (staging area):
```
    git rm --cashed script.js
```
* Сохранить изменения перед отправкой в репозиторий. Сообщение для commit написать в редакторе по умолчанию:
```
    git commit
```
* Сообщение для commit записывается в терминале:
```
    git commit -m "message"
```
* Изменить сообщение ("message") последнего commit:
``` 
    git commit --amend -m "new message"
```  
* Переход в определенную версию проекта по <commit hash>:
```
    git checkout <commit hash>
```
* Просмотреть изменения script.js:
```
    git log -p -- script.js
```
* Просмотреть log последних commit в одну строку:
```
    git log --oneline
```
* Просмотреть подробное содержание log в commit:
```
    git log --graph --oneline --all
```
* Просмотреть вывод log о каждом commit в одну строку:
```
    $ git log --pretty=oneline
```
* Просмотреть тип объекта Git по определенному <commit hash>:
```
    git cat-file -t <commit hash>
```
* Просмотреть содержание объекта Git по определенному <commit hash>:
```
    git cat-file -p <commit hash>
```
* Просмотреть какие изменения произошли в определенном commit:
```
    git show <commit hash>
```
* Просмотреть все ветки проекта:
```
    git branch
```
* Просмотреть все ветки проекта, включая те, которые находятся на удаленном репозитории:
```
    git branch -a
```
* Создать новую ветку проекта <branch name>:
```
    git branch <branch name>
```
* Переход в определенную версию проекта по названию ветки <branch name>:
```
    git checkout <branch name>
```
* Создать новую ветку проекта <branch name> и осуществить переход на неё:
```
    git checkout -b <branch name>
```
* Переименовать текущую ветку проекта <branch name>:
```
    git branch -m <new branch name>
```
* Удалить ветку проекта <branch name> после перехода на другую ветку:
```
    git branch -d <branch name>
```
* Слияние другой ветки (feature branch) в текущую ветку проекта <receiving branch>:
```
    git merge <feature branch name>
```
* Слияние другой ветки (feature branch) в текущую ветку проекта <receiving branch> с сообщением commit:
```
    git merge -m "message" <feature branch name>
```
* Клонирование удаленного репозитория в локальный:
```
    git clon <url>
```
* Загрузка и применение изменений с удаленной ветки репозитория в локальную:
```
    git pull
```
* Загрузка изменений из локальной ветки в удаленную ветку репозитория:
```
    git push
```
* Подключение удаленного репозитория:
```
    git remote add origin <url>
```
* Загрузка изменений из локальной ветки в удаленную ветку с созданием связи между ними:
```
    git push -u origin <branch>
```
* Проверка соединение локального и удаленного репозитория:
```
    git remote -v
```
* Проверка связи локальной и удаленной ветки репозитория:
```
    git branch -vv
```
* Переместить репозиторий в предыдущий commit, отбрасывая любые изменения:
```
    git reset
```
* Заменить все файлы в рабочей директории на последнюю версию, для который был выполнен commit:
```
    git reset --hard HEAD
```
* Поиск по ключевому слову в комментариях к commit:
```
    git log | grep -e "first"
```
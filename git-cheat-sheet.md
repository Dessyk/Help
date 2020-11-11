git add fileName - Добавляет untracked в stage area
git add . или git add --all - Добавить все файлы (Модифицированные и новые) в stage area

git checkout -b Test - Создает ветку и переключается на нее
git checkout -- Demo - Удаляет все изменения до последнего коммита в файле Demo
git checkout .  - Revert changes made to your working copy
git reset HEAD Demo - Удаляет файл Demo из Stage состояния

git clean -f - Remove untracked files

git reset --soft HEAD^
git reset --soft HEAD~1 - Выполняет операцию возврата предидущего коммита, для выполнения операций коммита доп. изменений
git reset --hard HEAD~1 (1 кол-во коммитов - можно 2,3 и т.д.)
git reset --hard HEAD^ - Выполняет отмену предыдущего коммита
git reset --hard HEAD^^ - Выполняет отмену двух предыдущих коммитов

git commit --amend -m "Test message" - Выполняет докоммит в предыдущий коммит (Переписывает сообщение коммита)
git commit -a -m "Commit message" - Добавляет все tracked файлы и выполняет коммит, но не добавляет untracked файлы
git commit -m "Commit message" - Выполняем коммит 

git diff - для unstage выведет разницу, а для staged нет
git diff --staged - выведет разницу для staged

git push origin feature/VT2.5UA - Отправляет локальную ветку в remote (даже без изменений в самой ветке)

git push origin :remote_branch - Удаляет remote branch, но оставляет локальный
git branch -d branchName - Удаляет локальную ветку (если есть изменения, удалить не даст)
git branch -D branchName - Удаляет локальную ветку

git remote show origin - Показывает привязку local branch to remote branch 

git remote prune origin - Чистит все удаленные Remote branches

git tag - Показать все теги
git checkout 2.5.032 - Достаем код на коммите с этим тегом
git tag -a 2.5.032 -m "Message" - Добавить новый тег
git push --tags - Push tags to remote(Иначе они будут только локально)

git stash save "Message"- Забрасывает в stash datasource все что было модифицированно (Message - опционально)
git stash save --keep-index - Забрасывает в stash datasource все что было модифицированно, но не трекается (unstage)????
git stash apply - Возвращает изменения из stash datasource
git stash apply stashName - Возвращает изменения из stash datasource по имени
git stash list - Показывает стек из стешей
git stash drop - Удаляет stash из stash datasource
git stash pop - Тоже самое что и git stash apply и потом git stash drop
git stash clear - Удалить все Stash-ы

Rebase 
git checkout branchName - Переключаемся в ветку 
git rebase master - Выполняем Rebase из ветки master
Вначале поставятся коммиты из мастер после этого по одному применятся коммиты из branchName

git rebase -i HEAD~3 - Выполняет интерактивный rebase (можно поменять порядок выполнения rebase, поменять сообщение в коммите)

Merge
git merge branchName - Выполяет мерж из ветки "branchName" в текущую ветку


git log --oneline --graph - Выводит визуальное представление веток
git log --pretty=oneline - Выводит историю коммитов, один коммит на строку

git blame fileName - Выводит Blame

git rm --cached fileName  - Прекращает трекать файл и удаляет из git, но не удаляет из файловой системы

git config --global alias.st status - выполняет сокращение

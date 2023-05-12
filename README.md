# GitHub. HW_2 
**1.** _На локальном репозитории сделать ветки для:_
```
- Postman 
- Jmeter 
- CheckLists 
- Bag Reports 
- SQL 
- Charles 
- Mobile testing 
```
  _Ветка создается командой_ `git branch _название ветки_`
  ```
$ git branch Postman
```
  _так же если  нужно создать много веток, то команду можно повторять через знак `&&`_
```
$ git branch Jmeter && git branch Checklist && git branch Bag_Reports && git branch SQL && git branch Charles && git branch Mobile_testing
```
**2.** _Запушить все ветки на внешний репозиторий_

_Командой_ `git push -u origin _название ветки_` _загружается на внешний репозиторий_
```
$ git push -u origin Postman
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Postman' on GitHub by visiting:
remote:      https://github.com/h1stav/test_branch/pull/new/Postman
remote:
To https://github.com/h1stav/test_branch.git
 * [new branch]      Postman -> Postman
branch 'Postman' set up to track 'origin/Postman'.
```
_p/c, так делаем с каждой веткой_

**3.** _В ветке **Bag Reports** сделать текстовый документ со структурой баг репорта_ 

_Для начала переходим в ветку **Bug_Reports**,_ _командой_ `git checkout _название ветки_`
```
$ git checkout Bag_Reports
```
Result
```
Already on 'Bag_Reports'
Your branch is up to date with 'origin/Bag_Reports'.
```
_Создаем текстовый документ через команду `cat >> _название файла`_
```
$ cat >> bag_reports.txt
ID
Severity
Title
Steps
Actual Result
Expected Result
Environment
Priority
```
**4.** _Запушить структуру багрепорта на внешний репозиторий_

_Сначала выполняем_ `git add .`

_Не забываем про команду_ `git commit -m _коментарий_`
```
$ git commit -m "bag reports"
[Bag_Reports b2389c2] bag reports
 1 file changed, 8 insertions(+)
 create mode 100644 bag_reports.txt
```
_Ну и послежний шаг чтобы запушить на внешний репозиторий, это команда_ `git push`
```
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 342.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/h1stav/test_branch.git
   883673d..b2389c2  Bag_Reports -> Bag_Reports
```
**5.** _Вмержить ветку **Bag Reports** в **Main**_ 

_Для того чтобы вмержить ветку `Bag Reports`, нужно сначала перейти на ту ветку, куда мы хотим ее вмержить_

_Для этого используем сначала команду_ `git checkout main`
```
$ git checkout main
```
Result
```
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
_А после уже используем команду_ `git merge Bag_Reports`
```
$ git merge Bag_Reports
```
Result
```
Updating 883673d..b2389c2
Fast-forward
 bag_reports.txt | 8 ++++++++
 1 file changed, 8 insertions(+)
 create mode 100644 bag_reports.txt
```
**6.** _Запушить **main** на внешний репозиторий_

_Делаем известной нами командой_ `git push`
```
$ git push
```
Result
```
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/h1stav/test_branch.git
   883673d..b2389c2  main -> main
```
**7.** _В ветке **CheckLists** набросать структуру чек листа_

_Для начала переходим в ветку **Checklist**,_ _командой_ `git checkout _название ветки_`
```
$ git checkout Checklist
```
Result
```
Switched to branch 'Checklist'
Your branch is up to date with 'origin/Checklist'.
```
_Создаем текстовый документ через команду `cat >> _название файла`_
```
$ cat >> check_attributes.txt
ID
Title
Precondition
Steps
Expected Result
```
**8.** _Запушить структуру на внешний репозиторий_ 
_Данное задание повторяется с 4 заданием, также можно попробовать написать команду в одну строку_
```
$ git add . && git commit -m "Checklist" && git push
```
Result
```
warning: in the working copy of 'check_attributes.txt', LF will be replaced by CRLF the next time Git touches it
[Checklist 89fe4cb] Checklist
 1 file changed, 5 insertions(+)
 create mode 100644 check_attributes.txt
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/h1stav/test_branch.git
   883673d..89fe4cb  Checklist -> Checklist
```
**9.** На внешнем репозитории сделать Pull Request ветки CheckLists в main 


**10.** Синхронизировать Внешнюю и Локальную ветки Main

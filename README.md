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
Git checkout название ветки

4. Запушить структуру багрепорта на внешний репозиторий
Git add .
Git commit -m “коментарий”
Git push

5. Вмержить ветку Bag Reports в Main 
Git checkout main
Git merge Bag_Reports

6. Запушить main на внешний репозиторий. 
Git push

7. В ветке CheckLists набросать структуру чек листа. 


8. Запушить структуру на внешний репозиторий 


9. На внешнем репозитории сделать Pull Request ветки CheckLists в main 


10. Синхронизировать Внешнюю и Локальную ветки Main

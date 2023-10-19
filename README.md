# LR6
***Лабораторная работа №6***
### Система контроля версий

Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# ***Основная часть***

> Замечания:
> В репозитории создана папка screen_folder, в которой хранятся все необходимые скриншоты. Имя скриншота начинается с ЛБ6, что указывает на принадлежность к данной лабораторной работе, число после " _ " указывает на номер скриншота.
> 
> Для нагляядности проделанной работы была создана ветка _Lab6_file_

### ***Шаг один***
Первый шаг заключался в том, чтобы создать аккаунт на GitHub (_См. screen_folder/ЛБ6_1.PNG_).

### ***Шаг два***
Далее необходимо было сделать	копию	репозиторию в	личное	хранилище	из _https://github.com/Kurtyanik/LR6/_. Это осуществвляется с помощью _Fork_ (_См. screen_folder/ЛБ6_2.PNG_ и _screen_folder/ЛБ6_3.PNG_). 

### ***Шаг три и шаг четыре***
Необходимо установить клиент Git, а затем настроить его, введя ФИО и электронную почту. Данные задачи осуществляются с помощью _git config --global user.name_ и _git config --global user.email_ (_См. screen_folder/ЛБ6_4.PNG_ и _screen_folder/ЛБ6_5.PNG_).

### ***Шаг пять***
Далее необходимо клонировать свой личный удалённый репозиторий на компьютер. Клонирование происходит в папку Lab6_OP, находящуюся на рабочем столе копьютера (_См. screen_folder/ЛБ6_6.PNG_).

### ***Шаг шесть***
Необходимо добавить	файл	через	интерфейс	GitHub и подтянуть	изменения	в локальный репозиторий (_См. screen_folder/ЛБ6_7.PNG_). На скриншоте ЛБ6_8 (_См. screen_folder/ЛБ6_8.PNG_) представлены составляющие локального репозитория до обновленния данных и после. Поиск составляющих производится с помощью _ls -1_. Подтягивание информации осуществляется с помощью _git pull_

### ***Шаг семь и восемь***
Нужно получить историю операций для веток и просмотреть последние изменения. Узнать какие ветки существуют можно с помощью _git branch_, чтобы получить историю операций над ветками можно использовать _git reflog (имя ветки)_. Для просмотра последних изменений используется функция _log_ (_См. screen_folder/ЛБ6_9.PNG_)

### ***Шаг девять***
Следующим шагом необходимо выполнить	слияние	в	ветку	_master_. Слияние происходит из ветки _Lab6_file_. На скриншоте ЛБ6_10 (_См. screen_folder/ЛБ6_10.PNG_) видно, что содержимое _Lab6_file_ добавилось в ветку _master_.

### ***Шаг десять***
Следующим шагом нужно удалить побочную ветку после успешного слияния. Делается это с помощью _git branch -d (имя ветки)_. В данном случае используется _git branch -d Lab6_file_ (_См. screen_folder/ЛБ6_11.PNG_).

### ***Шаг одиннадцать***
Для наглядной работы с репозиторием необходимо сделать изменения	и	зафиксировать	их,	оставляя	комментарии. Поочередно в репозиторий были добавлены три текстовых файла: _first.txt_, _second.txt_, _third.txt_. Они были сделаны с помощью _nano (имя файла).txt_. Что бы добавить изменения нужно воспользоваться _git add_, для создания коммита используется _git commit -m "(текст коммита)"_, для возвращения информации в репозиторий используется _git push_(_См. screen_folder/ЛБ6_12.PNG_, _См. screen_folder/ЛБ6_13.PNG_, _См. screen_folder/ЛБ6_14.PNG_).

### ***Шаг двенадцать***
Необходимо сделать откат коммита. Делается это с помощью _git revert HEAD --no-edit_( _См. screen_folder/ЛБ6_15.PNG_).

# ***Лог команд***
git config --global user.name "4218 Романькова Е. А."

git config --global user.email "euro1303@gmail.com"

cd Lab6_OP

git clone https://github.com/Ph1lls/LR6.git

ls -1

cd LR6

ls - 1

git pull

ls -1

git reflog

git log

git checkout Lab6_file

ls -1

git checkout master

ls -1

git merge Lab6_file

ls -1

git branch -d Lab6_file

nano first.txt

git status

git add first.txt

git status

git commit -m "Первое изменение"

git push

nano second.txt

git status

git add second.txt

git status

git commit -m "Второе изменение"

nano third.txt

git status

git add second.txt

git status

git push

git commit -m "Третье изменение"

git push

git revert HEAD --no-edit


# ***История операций***

commit b26ba7747361b644b6b7be04919d37338b366500 (HEAD -> master)
Merge: 397d8bd c664899
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Fri Oct 20 00:46:50 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit c664899bdc2be1dd01fb1feb58ddf69eb8cf740b (origin/master, origin/HEAD)
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:32:45 2023 +0300

    readme master branch

commit 21e38c85cf9bc6c8010a1e8979ce2f55202d3b6f
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:29:11 2023 +0300

    Add files via upload

    Добавлен сопровождающий скриншот к шагу 12

commit 21094b41ef13b91e24e2970b065cc51d68e0fada
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:23:39 2023 +0300

    Добавлен шаг 11

commit 9ea4c5521d40a8b0f9ac048c69fc4cb71d1ee437
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:21:52 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 11

commit 28f3c445870b42421c9487f23d8ba98f7abb3f92
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:10:36 2023 +0300

:...skipping...
commit b26ba7747361b644b6b7be04919d37338b366500 (HEAD -> master)
Merge: 397d8bd c664899
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Fri Oct 20 00:46:50 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit c664899bdc2be1dd01fb1feb58ddf69eb8cf740b (origin/master, origin/HEAD)
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:32:45 2023 +0300

    readme master branch

commit 21e38c85cf9bc6c8010a1e8979ce2f55202d3b6f
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:29:11 2023 +0300

    Add files via upload

    Добавлен сопровождающий скриншот к шагу 12

commit 21094b41ef13b91e24e2970b065cc51d68e0fada
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:23:39 2023 +0300

    Добавлен шаг 11

commit 9ea4c5521d40a8b0f9ac048c69fc4cb71d1ee437
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:21:52 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 11

commit 28f3c445870b42421c9487f23d8ba98f7abb3f92
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:10:36 2023 +0300

    Добавлены шаги 7, 8, 9 и 10, внесены небольшие изменения

commit 3e33ad2cfb072da95b705cdf69cc883822e53bfc
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:09:32 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагам 7, 8, 9 и 10
:...skipping...
commit b26ba7747361b644b6b7be04919d37338b366500 (HEAD -> master)
Merge: 397d8bd c664899
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Fri Oct 20 00:46:50 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit c664899bdc2be1dd01fb1feb58ddf69eb8cf740b (origin/master, origin/HEAD)
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:32:45 2023 +0300

    readme master branch

commit 21e38c85cf9bc6c8010a1e8979ce2f55202d3b6f
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:29:11 2023 +0300

    Add files via upload

    Добавлен сопровождающий скриншот к шагу 12

commit 21094b41ef13b91e24e2970b065cc51d68e0fada
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:23:39 2023 +0300

    Добавлен шаг 11

commit 9ea4c5521d40a8b0f9ac048c69fc4cb71d1ee437
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:21:52 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 11

commit 28f3c445870b42421c9487f23d8ba98f7abb3f92
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:10:36 2023 +0300

    Добавлены шаги 7, 8, 9 и 10, внесены небольшие изменения

commit 3e33ad2cfb072da95b705cdf69cc883822e53bfc
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:09:32 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагам 7, 8, 9 и 10

commit 397d8bd9767d94cb2d76072dabd7838c54ae4be1
Merge: 74bb40c 744523f
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 23:59:49 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit 744523fb78fe3c40d3171636cc8adf39a79e2120
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:51:10 2023 +0300

    Добавлены шаг 5 и шаг 6, внесены небольшие изменения в другие шаги

commit 8298eb10075683907dde53a59d08f58718976e5c
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:49:44 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 5 и шагу 6.

:
commit b26ba7747361b644b6b7be04919d37338b366500 (HEAD -> master)
Merge: 397d8bd c664899
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Fri Oct 20 00:46:50 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit c664899bdc2be1dd01fb1feb58ddf69eb8cf740b (origin/master, origin/HEAD)
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:32:45 2023 +0300

    readme master branch

commit 21e38c85cf9bc6c8010a1e8979ce2f55202d3b6f
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:29:11 2023 +0300

    Add files via upload

    Добавлен сопровождающий скриншот к шагу 12

commit 21094b41ef13b91e24e2970b065cc51d68e0fada
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:23:39 2023 +0300

    Добавлен шаг 11

commit 9ea4c5521d40a8b0f9ac048c69fc4cb71d1ee437
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:21:52 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 11

commit 28f3c445870b42421c9487f23d8ba98f7abb3f92
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:10:36 2023 +0300

    Добавлены шаги 7, 8, 9 и 10, внесены небольшие изменения

commit 3e33ad2cfb072da95b705cdf69cc883822e53bfc
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Fri Oct 20 00:09:32 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагам 7, 8, 9 и 10

commit 397d8bd9767d94cb2d76072dabd7838c54ae4be1
Merge: 74bb40c 744523f
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 23:59:49 2023 +0300

    Merge branch 'master' of https://github.com/Ph1lls/LR6

commit 744523fb78fe3c40d3171636cc8adf39a79e2120
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:51:10 2023 +0300

    Добавлены шаг 5 и шаг 6, внесены небольшие изменения в другие шаги

commit 8298eb10075683907dde53a59d08f58718976e5c
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:49:44 2023 +0300

    Add files via upload

    Добавлены сопровождающие скриншоты к шагу 5 и шагу 6.

commit f59a76fb116b1bffc24b44552367097906c21e02
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:34:06 2023 +0300

    Add files via upload

    Добавление сопровождающих скриншотов к шагу 3 и шагу 4

commit 9e48e1dd1fc408f687a59e3e3f613f203f78ccf8
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:30:35 2023 +0300

    Добавлено описание первого и второго шагов

commit 02d231d8239903573be7706cc1e890ce24a9a556
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:28:45 2023 +0300

    Add files via upload

    Добавление сопровождающих скриншотов к шагу 2

commit 6fc969b19fd5e6c8601e2600e55f6c92cb337753
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:22:20 2023 +0300

    Add files via upload

commit 97f2cb837572da8c46b34cc9776c16afbe3d7b77
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:13:49 2023 +0300

    Create folder

commit fc723852a5b55d9bcdc5f9d55d26fa8fb912b148
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:12:07 2023 +0300

    Delete screen_folder

commit e635c535b52185c7f0f814c977677ec02537f1c1
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 23:09:26 2023 +0300

    Create screen_folder

commit 74bb40c5cd3897bee9687bf4f41cdab81104a993
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 21:02:12 2023 +0300

    Revert "Третье изменение"

    This reverts commit 75f8c0deb67ca986f8ffc345e06f365b94af6243.

commit 75f8c0deb67ca986f8ffc345e06f365b94af6243
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 20:03:48 2023 +0300

    Третье изменение

commit edf6c336ca15b88decb29945ae6ee61ec69e384b
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 20:00:26 2023 +0300

    Второе изменение

commit ab2bcf68cd6f4e4cd840ef631fd8d9819d3231b5
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 19:57:49 2023 +0300

    Первое изменение

commit a2f6124314faf9d89ae85299b7c4a9a49810626b
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 19:43:36 2023 +0300

    Новый файл в ветке

commit 3922725527cf31ed5c9c32141cf0c5571b4d281b (origin/Lab6_file)
Author: 4218 Романькова Е. А. <euro1303@gmail.com>
Date:   Thu Oct 19 19:33:19 2023 +0300

    Внесены изменения в файл, добавлен комментарий

commit 5574a3e165cd1e68643828b03ade449c1c1e246f
Author: Ph1lls <113692843+Ph1lls@users.noreply.github.com>
Date:   Thu Oct 19 18:33:17 2023 +0300

    Create Lab6_file

    Added a new file

commit 921f53b8d0cebf542c791cf31f04e9b792f385a4
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:09:49 2020 +0300

    Обновление информации

commit c08a654a63cfc3a7146b2b7015884d9020f5cbf5
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:02:16 2020 +0300

    Файл создан пустым

commit 3c6e9131bb47ed6009c28226afb0535c7f6d5964
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 19:58:20 2020 +0300

    Initial commit


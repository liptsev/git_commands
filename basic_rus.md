# BASH  
dir //отображает список файлов в директории  
cd {dirname} //смена директории (/ - корневая папка, .. - на уровень выше)  
mkdir {dirname} //создание директории  
touch {filename} //создание файла  
echo ' ' > {filename} //перезапись файла  
cat {filename} //отображение текстового содержимого файла  
rm {filename} //удаление файла  
mv {filename} {newpath} //перемещение файла  
chmod ??? {filename} //смена прав на файл (для ExtN ф.с.)  
chown ??? {filename}//смена владельца файла (для ExtN ф.с.)  
  
# GIT BASIC  
git config --global user.name //задание имени пользователя  
git config --global user.email //задание почты пользователя  
git init //создание нового репозитория(внутри папки с именем репозитория)  
git log  
git status  
git add {filename} //добавление изменений/файла в индекс  
git add . //добавление всей папки в индекс  
git commit  
git commit -m ' '//коммит с описанием  
gitk //визуальный просмотрщик версий  
git clean -n //посмотреть локальные файлы на удаление  
git clean -fdx //удалить личные файлы  
git clone {http_link} //клонирует удаленный репозиторий в локальный  
git remote add origin {http_link} //связывает локальный репозиторий с удаленным  
git remote -v //отображает имена удаленных репозиториев и пути к ним  
git push // обновляет удаленный репозиторий из локального  
git push -f //перезаписывает удаленный репозиторий локальным  
git pull //получение данных из удаленного репозитория  
git rm //удаление файла из репозитория  
git mv {filename} {newpath} //перемещение файла
  
# GIT RESET  
head||index||filesystem  
git reset --soft {hash} //перезаписывает head  
git reset {hash} //перезаписывает индекс - потом можно закоммитить  
git reset --hard {hash} //перезаписывает и хедер и индекс и директорию: все незакоммиченные изменения восстановить невозможно, закоммиченные останутся с доступом по хешу, до уборки мусора из памяти  
git reset {filename} //отмена индексации файла: файл в индексе перезаписывается из последнего коммита(head)  
git reset {hash} {filename} //перезаписывает индекс определенного файла из определенного коммита  
  
# GIT CHECKOUT  
git checkout {hash} //переместиться к определенному хешу  
git checkout master //вернуться в основную ветку  
git checkout -b {new_branch_name} //создание новой ветки  
git tag //показать все метки  
git tag {tag_name} // установить новую метку  
git tag -d {tag_name} //удалить таг  
git checkout {tag_name} //переместиться к метке  
git checkout {filename} //перезаписать измененный файл версией из индекса  
  
git revert head/{hash}// отмена текущего/указанного коммита (информация об отмене отсается в логе)  
git commit --amend  //изменение текущего коммита(того на который ссылается HEAD)  
git branch (--merged, --no-merged) // посмотреть все ветки  
git branch {branch_name} //создание новой ветки  
git branch -d {branch_name} //удаление ветки  
git checkout {branch_name} //переключение между ветками  
git merge {branch_name} //слияние с веткой  
git mergetool //gui средство разрешения конфликтов при слиянии
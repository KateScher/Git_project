Урок 2. Работа с изменениями
Данное домашнее задание является продолжением домашнего задания, которое вы выполняли на предыдущем семинаре в репозитории с собственным проектом.

1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.

3. Попробуйте отменить эти три коммита:

- последний — командами git reset --soft и git restore;
- предпоследний — командой git reset --mixed и git restore;
- первый — командой git reset --hard.

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git log
commit fb53bb7804cfcda4c0cc3392ca78475dec8d9fcc (HEAD -> master, origin/master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:25:29 2023 +0500

    Change css file

commit 7313f881e62ba45d50ab36e85f751a86b3b88b3d
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:24:35 2023 +0500

    Change index2home

commit 2ebb9233458d6ffe39f37e3fde4d9b55a6603eb9
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:19:30 2023 +0500
:...skipping...
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:25:29 2023 +0500

    Change css file

commit 7313f881e62ba45d50ab36e85f751a86b3b88b3d
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:24:35 2023 +0500

    Change index2home

commit 2ebb9233458d6ffe39f37e3fde4d9b55a6603eb9
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:19:30 2023 +0500

    Change README.md file

commit 0bb2fb8833aa625ea5d1e90e452ed103716a16b3
Author: Ekaterina Scherbakova <kat-m1@mail.ru>

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git show fb53bb7
commit fb53bb7804cfcda4c0cc3392ca78475dec8d9fcc (HEAD -> master, origin/master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:25:29 2023 +0500

    Change css file

diff --git a/style2home.css b/style2home.css
index e3fd65c..59c1416 100644
--- a/style2home.css
+++ b/style2home.css
@@ -57,7 +57,7 @@ img {
border: 5px rgb(19, 208, 38) solid;
}
.bigtext {

- font-size: 2rem;

* font-size: 1.5rem;
  }
  margin-left: 50px;
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git show 7313f8
  commit 7313f881e62ba45d50ab36e85f751a86b3b88b3d
  Author: Ekaterina Scherbakova <kat-m1@mail.ru>
  Date: Sun Nov 19 18:24:35 2023 +0500

      Change index2home

diff --git a/index2home.html b/index2home.html
index 1eea30f..1a46e4e 100644
--- a/index2home.html
+++ b/index2home.html
@@ -38,6 +38,6 @@

<hr>
<a href="https://ru.wikihow.com/%D1%83%D1%85%D0%B0%D0%B6%D0%B8%D0%B2%D0%B0%D1%82%D1%8C-%D0%B7%D0%B0-%D1%81%D0%BE%D0%B1%D0%B0%D0%BA%D0%B0%D0%BC%D0%B8" target="_blank">Как ухаживать за собакой</a>
<hr>

-

* <p>Дрессировка также является неотъемлемой частью управления поведением собаки, ее воспитанием.</p>       
     </body>
   </html>
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git show 2ebb92
  commit 2ebb9233458d6ffe39f37e3fde4d9b55a6603eb9
  Author: Ekaterina Scherbakova <kat-m1@mail.ru>
  Date:   Sun Nov 19 18:19:30 2023 +0500

  Change README.md file

diff --git a/README.md b/README.md
index 8b13789..89409be 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,12 @@
+Урок 2. Работа с изменениями
+Данное домашнее задание является продолжением домашнего задания, которое вы выполняли на предыдущем семинаре в репозитории с собственным проектом.

+1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

- +2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.
- +3. Попробуйте отменить эти три коммита:
  Revert "Change README.md file" by task2 in homework
  Revert "Change index2home" by task 2 in homework
  Revert "Change css file" by task 2 in homework
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert 2ebb923
  [master 864e039] Revert "Change README.md file" by task2 in homework
  1 file changed, 11 deletions(-)
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert 7313f88
  [master 2f4d099] Revert "Change index2home" by task 2 in homework
  1 file changed, 1 insertion(+), 1 deletion(-)
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert fb53bb
  [master 85f2b7e] Revert "Change css file" by task 2 in homework
  1 file changed, 1 insertion(+), 1 deletion(-)
  PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> пше дщп
  пше : Имя "пше" не распознано как имя командлета, функции, файла сценария или выполняемой программы. Проверьте
  правильность написания имени, а также наличие и правильность пути, после чего повторите попытку.
  строка:1 знак:1
- пше дщп
- ```
    + CategoryInfo          : ObjectNotFound: (пше:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
  ```

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git log
commit 85f2b7e33bcc4b3826b595560da7495a635a2f34 (HEAD -> master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:02:07 2023 +0500

    Revert "Change css file" by task 2 in homework

    This reverts commit fb53bb7804cfcda4c0cc3392ca78475dec8d9fcc.

commit 2f4d09944090b5faec9be3f38d793994fe790bcd
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:01:11 2023 +0500

commit 85f2b7e33bcc4b3826b595560da7495a635a2f34 (HEAD -> master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:02:07 2023 +0500

    Revert "Change css file" by task 2 in homework

    This reverts commit fb53bb7804cfcda4c0cc3392ca78475dec8d9fcc.

commit 2f4d09944090b5faec9be3f38d793994fe790bcd
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:01:11 2023 +0500

:...skipping...
Date: Sun Nov 19 19:02:07 2023 +0500

    Revert "Change css file" by task 2 in homework

    This reverts commit fb53bb7804cfcda4c0cc3392ca78475dec8d9fcc.

Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:01:11 2023 +0500

    Revert "Change index2home" by task 2 in homework

commit 864e0398e9db806ed6a3084ce20e815ebfca0543
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 18:59:29 2023 +0500

    Revert "Change README.md file" by task2 in homework

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git reset --soft 85f2b7
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged README.md
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 3 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git push
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 1.09 KiB | 371.00 KiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/KateScher/Git_project.git
fb53bb7..85f2b7e master -> master
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status b7
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged style2home.css  
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git commit -m "Отмена коммита 3"
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md
modified: index2home.html
modified: style2home.css

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git add index2home.html
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
Your branch is up to date with 'origin/master'.

        modified:   index2home.html

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md
modified: style2home.css

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git commit -m "Change html file"
[master 2ce1e7b] Change html file
1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git add README.md
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
Your branch is ahead of 'origin/master' by 1 commit.
(use "git push" to publish your local commits)
(use "git restore --staged <file>..." to unstage)
modified: README.md
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: style2home.css

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git commit -m "Change md file"
[master 4e5241e] Change md file
1 file changed, 11 insertions(+)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git add style2home.css
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git commit -m "Change css file"
[master e3b4347] Change css file
1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git log
commit e3b4347cf40a3acd273676ec75d32b6f32e74a7e (HEAD -> master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:00:44 2023 +0500

    Change css file

commit 4e5241e6806aff1d2f7960579ad5be06f6a5ea45
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:00:05 2023 +0500

    Change md file

commit 2ce1e7b2aafd377865cd3f7e0c707f1e4b67e00c
:...skipping...

# with '#' will be ignored, and an empty message aborts the commit.

Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:00:44 2023 +0500
Revert "Change md file"
Change css file

Revert "Change html file"
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:00:05 2023 +0500
Change md file

commit 2ce1e7b2aafd377865cd3f7e0c707f1e4b67e00c
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:59:24 2023 +0500

    Change html file

commit 85f2b7e33bcc4b3826b595560da7495a635a2f34 (origin/master)
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 19:02:07 2023 +0500
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert e3b434
[master 69a5085] Revert "Change css file"
1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert 4e5241e
[master 6719b21] Revert "Change md file"
1 file changed, 11 deletions(-)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git revert 2ce1e7b2
[master 5b0748a] Revert "Change html file"
1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git log
Date: Sun Nov 19 20:04:59 2023 +0500

    Revert "Change html file"

    This reverts commit 2ce1e7b2aafd377865cd3f7e0c707f1e4b67e00c.

commit 6719b21428b28df7f79c298c30d52aefe3ed00b7
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:04:31 2023 +0500
Revert "Change md file"

    This reverts commit 4e5241e6806aff1d2f7960579ad5be06f6a5ea45.

commit 69a5085b7f5e1ee945062faec5dfdf5da074da2a
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:03:38 2023 +0500

    Revert "Change css file"

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git reset --soft 5b0748a6
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 6 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged index2home.html  
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 6 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git log  
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:04:59 2023 +0500
This reverts commit 2ce1e7b2aafd377865cd3f7e0c707f1e4b67e00c.

commit 6719b21428b28df7f79c298c30d52aefe3ed00b7
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:04:31 2023 +0500

    Revert "Change md file"

    This reverts commit 4e5241e6806aff1d2f7960579ad5be06f6a5ea45.

commit 69a5085b7f5e1ee945062faec5dfdf5da074da2a
Author: Ekaterina Scherbakova <kat-m1@mail.ru>
Date: Sun Nov 19 20:03:38 2023 +0500

    Revert "Change css file"

    This reverts commit e3b4347cf40a3acd273676ec75d32b6f32e74a7e.

PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git reset --mixed 6719b21
Unstaged changes after reset:
M index2home.html
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged index2home.html  
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged README.md
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index2home.html
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore --staged index2home.html  
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 5 commits.
(use "git push" to publish your local commits)
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index2home.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore index2home.html
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 5 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git restore README.md
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git status
On branch master
Your branch is ahead of 'origin/master' by 5 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project> git reset --hard 69a5085b7
HEAD is now at 69a5085 Revert "Change css file"
PS C:\Users\Екатерина\GB\Контроль версий GIT, углубленно\Git_project>

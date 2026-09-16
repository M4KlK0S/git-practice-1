<<<<<<< HEAD
<<<<<<< HEAD
# \# git-practice-1

# 

# Практическое задание по Git. Первый коммит.

=======
# git-practice-1

**1. Регистрация аккаунта на GitHub**

Выполнено ранее. Аккаунт GitHub уже зарегистрирован, веду собственные репозитории.

Примечание: если аккаунт новый — регистрация выполняется на https://github.com/signup с указанием email, имени пользователя и пароля.

**2. Создание нового публичного репозитория**

Действия:
- Открыл https://github.com/new.
- Указал Repository name (например, git-practice-1).
- Выбрал тип репозитория — Public.
- Поставил галочку «Add a README file» (в интерфейсе GitHub это поле называется «Initialize this repository with a README»).
- Нажал Create repository.

Результат: создан публичный репозиторий с автоматически сгенерированным файлом README.md и веткой main (или master — зависит от настроек аккаунта).

**3. Клонирование репозитория по HTTPS**

Скопировал URL репозитория (кнопка Code → HTTPS).
bash
git clone https://github.com/<username>/git-practice-1.git
Вывод (пример):

text
Cloning into 'git-practice-1'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Шаг 4. Переход в каталог с клоном
bash
cd git-practice-1
Шаг 5. Первоначальная настройка Git
Указал своё настоящее имя и email (глобально, для всех репозиториев):

bash
git config --global user.name "Ivan Ivanov"
git config --global user.email "johndoe@example.com"
Проверка настроек:

bash
git config --global --list
Вывод:

text
user.name=Ivan Ivanov
user.email=johndoe@example.com
Шаг 6. Первый вызов git status
bash
git status
Вывод:

text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
Пояснение: рабочая директория чистая — все файлы соответствуют последнему коммиту, изменений нет.

Шаг 7. Редактирование README.md
Открыл файл README.md в текстовом редакторе и добавил строку, например:

markdown
# git-practice-1

Практическое задание по Git. Первый коммит.
Сохранил файл. Файл перешёл в состояние Modified.

Шаг 8. git status после редактирования
bash
git status
Вывод:

text
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Пояснение: Git видит, что README.md изменён, но пока не добавлен в индекс (staging area).

Шаг 9. Просмотр изменений: git diff и git diff --staged
До добавления в индекс:

bash
git diff
Вывод (сокращённо):

text
diff --git a/README.md b/README.md
index e69de29..7c1f4b8 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,3 @@
+# git-practice-1
+
+Практическое задание по Git. Первый коммит.
После добавления в индекс пока ничего не staged, поэтому:

bash
git diff --staged
Вывод: пустой — индекс совпадает с HEAD.

Шаг 10. Добавление файла в индекс (staged)
bash
git add README.md
Проверка статуса:

bash
git status
Вывод:

text
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
Файл перешёл в состояние Staged.

Шаг 11. Повторные git diff и git diff --staged
bash
git diff
Вывод: пустой — рабочая директория совпадает с индексом.

bash
git diff --staged
Вывод: показывает те же изменения, что и раньше git diff, но теперь они находятся в индексе (готовы к коммиту):

text
diff --git a/README.md b/README.md
index e69de29..7c1f4b8 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,3 @@
+# git-practice-1
+
+Практическое задание по Git. Первый коммит.
Шаг 12. Создание коммита
bash
git commit -m 'First commit'
Вывод:

text
[main 4f3c2a1] First commit
 1 file changed, 3 insertions(+)
Проверка:

bash
git status
text
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
Шаг 13. Отправка изменений на GitHub
Так как GitHub по умолчанию создаёт ветку main, отправляем именно её:

bash
git push origin main
Вывод:

text
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 275 bytes | 275.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/<username>/git-practice-1.git
   7a1b2c3..4f3c2a1  main -> main
Если в вашем репозитории ветка называется master, команда будет:

bash
git push origin master
Переименовать ветку можно командой:

bash
git branch -M main
Проверка: открыл страницу репозитория на GitHub — файл README.md содержит новые строки, история коммитов показывает First commit.
>>>>>>> 0442b01b72d0638432276bed63e9e84a08c4921b
=======

>>>>>>> 89c81430faf3046ed3fd3a7e97b8424b1e4f04ba

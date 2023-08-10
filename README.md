# Команды для использования git через консоль

Чтобы вывести текущую рабочую директорию, используют команду `pwd`:

```
$ pwd
/c/Users/%USERNAME%
```

Чтобы перейти к домашней директории, используют команду `cd ~`:

```
$ cd ~
```

Выводить содержимое директорий с помощью `ls`:

```
$ ls
 Desktop/
 Documents/
 Downloads/
 IdeaProjects
 ...
```

Чтобы создать файл, нужно ввести в консоль команду `touch`:

```
$ touch my-new-file.txt
```

Для создания директорий через терминал используют команду `mkdir`:

```
$ mkdir new-dir
```

Для копирования файлов через терминал существует команда `cp`:

```
$ cp что_копируем куда_копируем

$ cp index.html src/
```

- Перемещение файлов и папок — `mv`:

```
$ mv table.csv ./very-important-files
# сначала указываем имя файла, который хотим переместить, потом путь — куда перемещаем
```

Чтобы прочитать файл, в консоль нужно ввести `cat` вместе с именем файла:

```
$ cat myfile.txt # распечатали содержимое файла myfile.txt
file-content-1
file-content-2
```

Чтобы удалить файл, нужно напечатать команду `rm` и передать ей имя файла:

```
$ rm example.txt # удалили файл example.txt из текущей папки
```

Удалить папку можно командой `rmdir`:

```
$ rmdir images # команда удалит папку images из текущей директории, если папка images пуста
```

# Хеш

**Хеширование** (от англ. _hash_, «рубить», «крошить», «мешанина») — это способ преобразовать набор данных и получить их «отпечаток» (англ. _fingerprint_).

Git хранит таблицу соответствий `хеш → информация о коммите`. Если вы знаете хеш, вы можете узнать всё остальное.
Все хеши и таблицу `хеш → информация о коммите` Git сохраняет в служебные файлы. Они находятся в скрытой папке `.git` в репозитории проекта.

# Лог

**Получить сокращённый лог —** `git log --oneline`.
В сокращённом логе выводятся сокращённые хеши — их можно использовать точно так же, как и полные.

# Файл `HEAD`

Файл `HEAD` (англ. «голова», «головной») — один из служебных файлов папки `.git`. Он указывает на коммит, который сделан последним (то есть на самый новый).

# Статусы файлов в Git

* `untracked` (англ. «неотслеживаемый»).
 У untrackedфайла нет предыдущих версий, зафиксированных в коммитах или через команду git add.
* `staged` (англ. «подготовленный»).
 После выполнения команды git add файл попадает в staging area (от англ. stage — «сцена», «этап [процесса]» и area — «область»), то есть в список файлов, которые войдут в коммит.
* `tracked` (англ. «отслеживаемый»).
 В статус попадают файлы, которые уже были зафиксированы с помощью git commit, а также файлы, которые были добавлены в staging area командой git add. То есть все файлы, в которых Git так или иначе отслеживает изменения.
* `modified` (англ. «изменённый»).
 Состояние `modified` означает, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия. Например, файл был закоммичен и после этого изменён.

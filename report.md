## Задание 1 - Автоматизация проверки формата файлов при коммите
# Отчет по заданиям

### Шаги выполнения
1. Для автоматической проверки перед коммитом создаем файл `pre-commit` в директории `.git/hooks/`. Этот файл будет выполнять проверку всех `.txt` файлов на наличие текста и подписи автора.

2. Внутри скрипта проверяется каждый измененный `.txt` файл на:
   - Пустоту.
   - Наличие строки, содержащей подпись автора.

3. Протестировал работу скрипта. Убедился, что если остутстует подпись автора, то коммит не будет происходить. 

## Задание 2 - Использование Git Flow в проекте

1. Установил git flow с помощью команды 
   ```
   sudo apt install git-flow
   ```
2. Инициализировал репозиторий с помощью команды 
   ```
   git flow init
   ```
3. Создал ветку для новой функциональности 
   ```
   git flow feature start task-management
   ```
4. Создал task_manager.py и закоммитил его 
   ```
   git add task_manager.py
   git commit -m "Добавлен task_manager.py"
   ```
5. Завершил все работы, слил ветку с веткой develop
   ```
   git flow feature finish task-management
   ```
6. Создал релиз
   ```
   git flow release start v1.0.0
   ```
7. Обновил версию в version.txt
8. Завершил релиз 
   ```
   git flow release finish v1.0.0
   ```
9. Исправление ошибок с hotfix 
   ```
   git flow hotfix start hotfix-1.0.1
   git add file_with_error.py
   git commit -m "Исправлена ошибка"
   git flow hotfix finish hotfix-1.0.1
   ```
10. Отправка в удаленный репозиторий 
   ```
   git push origin develop
   git push origin main
   ``` 

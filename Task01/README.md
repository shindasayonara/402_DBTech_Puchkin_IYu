# Проект "Сапер" (Minesweeper)

## Описание проекта

Проект включает разработку игры "Сапер" (Minesweeper) с использованием реляционной базы данных для сохранения результатов игр. Игра будет реализована с использованием PHP и SQLite. Также будет предусмотрена возможность просмотра истории игр и повторения ранее сыгранных партий.

## Задача для первого блока

### Вариант 5

Разработать программу для игры "Сапер" (Minesweeper). Игра проходит на квадратном игровом поле, которое разделено на смежные ячейки. Некоторые из этих ячеек заминированы; количество заминированных ячеек известно заранее. Цель игры - открыть все ячейки, не содержащие мины. Игрок открывает ячейки, стараясь не открыть ячейку с миной. Открыв ячейку с миной, он проигрывает. Если под открытой ячейкой мины нет, то в ней появляется число, показывающее, сколько ячеек, соседствующих с только что открытой, заминировано. Если под соседними ячейками тоже нет мин, то открывается не заминированная область до ячеек, в которых есть цифры. 

### Правила игры

- Игрок открывает ячейки, стараясь не открыть ячейку с миной. Если открывается ячейка с миной, игрок проигрывает.
- Если под открытой ячейкой мины нет, то в ней отображается число, показывающее количество соседних ячеек, содержащих мины.
- Если в соседних ячейках тоже нет мин, то открывается область до ячеек с цифрами.

### Требования

- **Размерность поля и количество мин**: Пользователь вводит эти параметры при запуске игры.
- **Сохранение данных**: Информация о датах и исходах всех партий, а также о всех ходах, сделанных во время игры, должна сохраняться в базе данных SQLite.
- **Хранение данных**: Для каждой игры в базе данных должна храниться следующая информация:
  - Дата игры
  - Имя игрока
  - Размерность поля и количество мин на поле
  - Расстановка мин на поле
  - Исход игры
  - Запись ходов в формате: `номер хода | координаты точки | результат (мины нет/взорвался/выиграл)`
- **Режимы игры**:
  - Новая игра
  - Вывод списка всех сохраненных партий
  - Повтор любой сохраненной партии (воспроизведение всех ходов из этой партии)

## Инструкция по запуску

1. **Настройка окружения**:
   - Убедитесь, что у вас установлены PHP и SQLite.
   - Для Windows: настройте переменные окружения для SQLite.
   - Для Unix-подобных систем: установите SQLite и сделайте скрипты исполняемыми.

2. **Запуск программы**:
   - Запустите скрипт для запуска игры (например, через командную строку или терминал).

3. **Инструкция по запуску скриптов**:
   - Для Windows: см. `README_logger.md` для инструкций по запуску `self-logger.bat`.
   - Для Unix-подобных систем: см. `README_logger.md` для инструкций по запуску `self-logger.sh`.

4. **Запуск PHP-скрипта**:
   - Используйте команду `php task1.php` для получения инструкции к игре.

## Примечания

- Убедитесь, что у вас есть права на запись в директорию, где находятся базы данных SQLite.
- Для дополнительной помощи обратитесь к документации SQLite или PHP.


---

Ссылки на документацию:
- [SQLite Documentation](https://www.sqlite.org/docs.html)
- [PHP Documentation](https://www.php.net/docs.php)

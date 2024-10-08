# GitHub Gists list

Тестовое задание для вакансии iOS Разработчик в комнанию **Astrosoft**.

## Описание ТЗ

Приложение для чтения (отображения) списка гистов с открытого api github, с возможноестью просмотреть подробную информацию.
Приложение имеет два экрана
- список гистов;
- подробная информация по гисту;

## Требования

Готовое приложение, способное запросить, отобразить список гистов и так же показать всю информацию по гисту.
При разработке нужно использовать язык программирования `Swift`, без использования `Storyboard` и `Xib`.

[Документация по api](https://docs.github.com/en/rest/gists/gists?apiVersion=2022-11-28#about-gists).

Результаты принимаются только как репозиторий на gitHub. Для удобства, можно сдлеать форк от данного репозитория.
Присылать на sgaponov@astrosoft.ru.

### Первый экран приложения

Список гистов, полученных по api

**UI:**
- UITableView;
- ячейка отображает:
    - аватар автора;
    - название гиста;
    - имя автора;

**Реализованно:**
- `pull to refresh`;
- пагинация;
- разрмеры ячейки рассчитываются автоматически
- переход на следующий экран по нажатию на гист

### Второй экран приложения

Подробная информация по выбранному гисту

**UI**
- UICollectionView;
- Отображается:
    - аватар + имя автора;
    - название гиста;
    - гист (т.к в гисте может быть несколько файлов, то нужно отобразить каждый гист, но не более 5 строк);
    - список коммитов, менявших этот гист;

**Реализованно**
- `pull to refresh`;
- разрмеры ячейки рассчитываются автоматически;
- При нажатии на файл, отображается полный содержание файла через present (в самом простом виде).

### Общие требования
- архитектура VIPER/MVVM
- Использовать кеширование для картинок. Как именно - на свое усмотрение;
- Загрузка данных - не использовать Alamofire и подобное. Нативная загрузка данных;
- Показать навыки использования: 
    - protocol;
    - extensions;
    - struct;
    - encode/decode;
    - диспетчиризации;

### Дополнительно/по желанию
- поддержка темной темы

## **UPDATE**

При работе лучше использовать Xcode версии не выше 15.4. Если такой возможности нет, и проект создан на Xcode 16, то потребуются дополнительные манипуляции, для запуска проекта на 15.4.

Что нужно будет сделать
- [Установить версию проекта](https://forums.developer.apple.com/forums/thread/689451)
- [Обернуть папки в группы](https://blog.supereasyapps.com/xcode-16-buildable-folders-break-xcode-15-backwards-compatibility/)

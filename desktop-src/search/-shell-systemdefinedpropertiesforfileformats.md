---
description: Microsoft Windows предоставляет ряд системных свойств, которые можно использовать для форматов файлов.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Свойства System-Defined для пользовательских форматов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28dcf137d10fffb3cc192acf66b1279b83fd079b6b81cf963dfed8a78408388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944504"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>Свойства System-Defined для пользовательских форматов файлов

Microsoft Windows предоставляет ряд системных свойств, которые можно использовать для форматов файлов. При создании пользовательского формата файла необходимо поддерживать как можно больше системных свойств. Перед созданием обработчика настраиваемого свойства необходимо просмотреть обработчики, предоставляемые системой, чтобы определить, можно ли использовать его вместо написания собственного.

В следующей таблице приведены категории форматов файлов, а затем перечислены наиболее важные системные свойства, которые должен поддерживать ваш формат файла. Чтобы обеспечить хорошую работу пользователей, необходимо поддерживать все свойства приоритета 1 и 2 для категории формата файлов.

-   [Операции взаимодействия](#communications)
-   [Контакты](#contacts)
-   [Документы](#documents)
-   [Универсальный шаблон](#generic)
-   [Музыка](#music)
-   [Рисунки](#pictures)
-   [Видео](#videos)
-   [Связанные темы](#related-topics)

## <a name="communications"></a>Коммуникации



| Имя            | Свойство                               | Приоритет |
|-----------------|----------------------------------------|----------|
| Дата получения   | System. Message. Датерецеивед            | 1        |
| Из имен      | System. Message. Фромнаме                | 1        |
| Имеет вложения | System. Message. Хасаттачментс          | 1        |
| Mailbox         | System. Communication. стореддисплайнаме | 1        |
| name            | System. имя_файла                        | 1        |
| Тема         | System. subject                         | 1        |
| В имена        | System. Message. Тонаме                  | 1        |
| Категория        | System. Category                        | 2        |
| Тип            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Контакты



| Имя             | Свойство                           | Приоритет |
|------------------|------------------------------------|----------|
| Имя учетной записи     | System. Communication. AccountName   | 1        |
| Business Phone   | System. Contact. Бусинесстелефоне   | 1        |
| Company          | System. Company                     | 1        |
| Электронная почта    | System. Contact. Примаремаиладдресс | 1        |
| Важность       | System. Импортанцетекст              | 1        |
| Мобильный телефон     | System. Contact. Мобилетелефоне     | 1        |
| Рабочий адрес | System. Contact. Бусинессаддресс     | 2        |
| Бизнес-Факс     | System. Contact. Бусинессфакснумбер   | 2        |
| Категория         | System. Category                    | 2        |
| Домашний адрес     | System. Contact. HomeAddress         | 2        |
| Домашний телефон       | System. Contact. Хометелефоне       | 2        |
| Название            | System.Title                       | 2        |



 

## <a name="documents"></a>Документы



| Имя      | Свойство             | Приоритет |
|-----------|----------------------|----------|
| Авторы   | System.Author        | 1        |
| Полнотекстовый | System. FullText      | 1        |
| Теги      | System.Keywords      | 1        |
| Тип      | System.PerceivedType | 1        |
| Категория  | System. Category      | 2        |
| Название     | System.Title         | 2        |



 

## <a name="generic"></a>Универсальный шаблон



| Имя     | Свойство             | Приоритет |
|----------|----------------------|----------|
| Авторы  | System.Author        | 1        |
| Название    | System.Title         | 1        |
| Тип     | System.PerceivedType | 1        |
| Категория | System. Category      | 2        |
| Теги     | System.Keywords      | 2        |



 

## <a name="music"></a>Музыка



| Имя         | Свойство                     | Приоритет |
|--------------|------------------------------|----------|
| \#           | System. Music. Траккнумбер     | 1        |
| Album        | System. Music. Албумтитле      | 1        |
| Исполнител      | System. Music. исполнителя          | 1        |
| Genre        | System. Music. Жанр           | 1        |
| Рейтинг       | System. Оценка                | 1        |
| Название        | System.Title                 | 1        |
| Исполнитель альбома | System. Music. Албумартист     | 2        |
| Скорость     | System. Audio. Енкодингбитрате | 2        |
| Поведения   | System. Music. Проводник       | 2        |
| Длина       | System. Media. Duration        | 2        |
| Защищенный    | System. DRM. для защиты       | 2        |
| Year;         | System. Media. Year            | 2        |



 

## <a name="pictures"></a>Изображения



| Имя          | Свойство                        | Приоритет |
|---------------|---------------------------------|----------|
| Дата импорта | System. Датеимпортед             | 1        |
| Дата съемки    | System. photo. Датетакен          | 1        |
| Рейтинг        | System. Оценка                   | 1        |
| Теги          | System.Keywords                 | 1        |
| Тип          | System.PerceivedType            | 1        |
| Авторы       | System.Author                   | 2        |
| Камера, изготовитель  | System. photo. Камерамануфактурер | 2        |
| Модель камеры  | System. photo. Камерамодел        | 2        |
| Примечания      | System. комментарий                  | 2        |
| Измерения    | System. Image. Dimensions         | 2        |



 

## <a name="videos"></a>Видео



| Имя         | Свойство                 | Приоритет |
|--------------|--------------------------|----------|
| Длина       | System. Media. Duration    | 1        |
| Рейтинг       | System. Оценка            | 1        |
| Теги         | System.Keywords          | 1        |
| Тип         | System.PerceivedType     | 1        |
| Высота рамки | System. Video. Фрамехеигхт | 2        |
| Ширина рамки  | System. Video. Фрамевидс  | 2        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[разработка обработчиков свойств для Windows поиска](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Система свойств](../properties/building-property-handlers.md)
</dt> <dt>

[Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 

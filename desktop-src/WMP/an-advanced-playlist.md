---
title: Расширенный список воспроизведения
description: Расширенный список воспроизведения
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows Списки воспроизведения метафайлов мультимедиа, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Windows Списки воспроизведения мультимедийных метафайлов, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Windows Списки воспроизведения метафайлов мультимедиа, примеры списков воспроизведения
- списки воспроизведения, образцы списков воспроизведения
- списки воспроизведения метафайлов, образцы списков воспроизведения
- Windows Списки воспроизведения мультимедийных метафайлов, пример кода
- списки воспроизведения, пример кода
- списки воспроизведения метафайлов, пример кода
- Windows Списки воспроизведения метафайлов мультимедиа, пример расширенного списка воспроизведения
- списки воспроизведения, пример расширенного списка воспроизведения
- списки воспроизведения метафайлов, пример расширенного списка воспроизведения
- проигрыватель Windows Media, примеры списков воспроизведения
- проигрыватель Windows Media, примеры списков воспроизведения
- проигрыватель Windows Media, образцы списков воспроизведения
- проигрыватель Windows Media, пример расширенного списка воспроизведения
- примеры списков воспроизведения
- примеры списков воспроизведения
- Образцы списков воспроизведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583261"
---
# <a name="an-advanced-playlist"></a>Расширенный список воспроизведения

В следующем примере списка воспроизведения показано, как использовать более полный набор элементов списка воспроизведения. при написании собственного кода необходимо изменить все url-адреса и имена файлов на допустимые имена файлов, доступные для проигрыватель Windows Media.

Пример кода


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



В следующей таблице описаны предыдущие дополнительные списки воспроизведения.



| Линия                                                                                            | Описание                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | элемент [ASX](asx-element.md) идентифицирует клиент (проигрыватель Windows Media), что это Windows списка воспроизведения метафайла мультимедиа. Атрибут **Version** указывает номер версии элементов метафайла.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | Элемент [Title](title-element--metafile.md) определяет заголовок списка воспроизведения в целом. проигрыватель Windows Media отображает эти метаданные в качестве заголовка для отображения.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | [Абстрактный](abstract-element.md) элемент предоставляет подсказку для заголовка отображения.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | Элемент [мореинфо](moreinfo-element.md) связывает заголовок "показывать" с URL-адресом. При наведении указателя мыши на заголовок Показывать подсказку, если она определена. При выборе пункта "показывать" заданный URL-адрес будет открыт.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | элемент [баннера](banner-element.md) создает баннер объявления в проигрыватель Windows Media. Атрибут **href** указывает рисунок баннера (Ширина 194 пикселей в ширину составляет 32 пикселей в высоту).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | [Абстрактный](abstract-element.md) элемент предоставляет подсказку для **баннера**.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | Элемент [мореинфо](moreinfo-element.md) связывает изображение **баннера** с URL-адресом. Наведение указателя мыши на **баннер** обращается к подсказке, если она определена. При выборе **баннера** будет открыт указанный URL-адрес.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | Элемент [param](param-element.md) определяет пользовательский параметр. Атрибут **Name** определяет имя пользовательского параметра как Track. Атрибут **value** определяет значение "Track", равное "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Закрывает элемент **баннера**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Начинает блок элемента [entry](entry-element.md) . Этот элемент определяет клип в списке воспроизведения, указывая ссылку в элементе **ref** . Если для параметра **клиентскип** задать значение "нет", то пользователь не сможет выполнить перемотку вперед или перейти к следующему клипу                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Создает баннер объявления. **Href** — это рисунок баннера (194x32 пикселей).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Предоставляет подсказку для баннера.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Содержит ссылку на URL-адрес баннера. При выборе баннера подключается к URL-адресу.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Закрывает элемент **баннера**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Содержит ссылку на URL-адрес для текста **заголовка** клипа.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Примечание. [Комментарии](comments.md) отображаются только при просмотре кода.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Предоставляет подсказку для текста **заголовка** клипа.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Определяет заголовок клипа. Это **заголовок** клипа, так как он вложен в элемент **entry** . проигрыватель Windows Media отображает эти метаданные в качестве заголовка клипа.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Определяет автора клипа мультимедиа. эти метаданные отображаются как **автор** клипа проигрыватель Windows Media.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | Элемент [Copyright](copyright-element.md) указывает авторские права, связанные с клипом мультимедиа. проигрыватель Windows Media отображает эти метаданные в качестве обрезки авторские права.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Комментарий в том же формате, что и **XML-** комментарии.                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL-адрес мультимедийного содержимого. Элемент [ref](ref-element.md) определяет строку как указатель на мультимедийное содержимое. Атрибут **href** является URL-адресом файла. Обратите внимание на использование закрытия элемента, похожего на XML, "/>" вместо " &lt; /реф &gt; ". Поскольку этот элемент не имеет дочерних элементов, он закрывается.<br/> |
| `</ENTRY>`                                                                                  | Задает конец первого элемента **entry** .                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Начинает второй элемент **entry** .                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Определяет заголовок второго клипа.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Определяет автора второго клипа мультимедиа.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Примечание. Он будет отображаться только при просмотре кода.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Это текст подсказки для текста **заголовка** клипа.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Примечание. Он будет отображаться только при просмотре кода.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Определяет строку как указатель на мультимедийное содержимое. Атрибут **href** является URL-адресом файла.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Задает конец второго элемента **entry** .                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Указывает конец списка воспроизведения.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание списков воспроизведения метафайлов**](creating-metafile-playlists.md)
</dt> <dt>

[**Примеры списков воспроизведения**](example-playlists.md)
</dt> <dt>

[**Списки воспроизведения метафайлов**](metafile-playlists.md)
</dt> <dt>

[**Windows Справочник по элементам метафайлов мультимедиа**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Мультимедийное по для метафайлов**](windows-media-metafile-guide.md)
</dt> </dl>

 

 






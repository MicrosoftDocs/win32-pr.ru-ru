---
title: Расширенный список воспроизведения
description: Расширенный список воспроизведения
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, образцы списков воспроизведения
- списки воспроизведения метафайлов, образцы списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, пример кода
- списки воспроизведения, пример кода
- списки воспроизведения метафайлов, пример кода
- Списки воспроизведения метафайлов Windows Media, пример расширенного списка воспроизведения
- списки воспроизведения, пример расширенного списка воспроизведения
- списки воспроизведения метафайлов, пример расширенного списка воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, образцы списков воспроизведения
- Проигрыватель Windows Media, пример расширенного списка воспроизведения
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067764"
---
# <a name="an-advanced-playlist"></a>Расширенный список воспроизведения

В следующем примере списка воспроизведения показано, как использовать более полный набор элементов списка воспроизведения. При написании собственного кода необходимо изменить все URL-адреса и имена файлов на допустимые имена файлов, доступные проигрывателю Windows Media.

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
| `<ASX version = "3.0">`                                                                     | Элемент [ASX](asx-element.md) определяет для клиента (проигрыватель Windows Media), что это список воспроизведения метафайла Windows Media. Атрибут **Version** указывает номер версии элементов метафайла.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | Элемент [Title](title-element--metafile.md) определяет заголовок списка воспроизведения в целом. Проигрыватель Windows Media отображает эти метаданные в качестве заголовка для отображения.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | [Абстрактный](abstract-element.md) элемент предоставляет подсказку для заголовка отображения.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | Элемент [мореинфо](moreinfo-element.md) связывает заголовок "показывать" с URL-адресом. При наведении указателя мыши на заголовок Показывать подсказку, если она определена. При выборе пункта "показывать" заданный URL-адрес будет открыт.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | Элемент [баннера](banner-element.md) создает баннер рекламного объявления в проигрывателе Windows Media. Атрибут **href** указывает рисунок баннера (Ширина 194 пикселей в ширину составляет 32 пикселей в высоту).                                                                                                                                  |
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
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Определяет заголовок клипа. Это **заголовок** клипа, так как он вложен в элемент **entry** . Проигрыватель Windows Media отображает эти метаданные как заголовок клипа.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Определяет автора клипа мультимедиа. Эти метаданные отображаются проигрывателем Windows Media как **Автор** клипа.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | Элемент [Copyright](copyright-element.md) указывает авторские права, связанные с клипом мультимедиа. Проигрыватель Windows Media отображает эти метаданные в виде обрезки АВТОРских прав.                                                                                                                                                              |
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание списков воспроизведения метафайлов**](creating-metafile-playlists.md)
</dt> <dt>

[**Примеры списков воспроизведения**](example-playlists.md)
</dt> <dt>

[**Списки воспроизведения метафайлов**](metafile-playlists.md)
</dt> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Путеводитель по метафайлу Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 






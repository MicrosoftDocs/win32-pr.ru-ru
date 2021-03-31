---
title: Использование пользовательских параметров и команд
description: Использование пользовательских параметров и команд
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Списки воспроизведения метафайлов Windows Media, пользовательские параметры
- списки воспроизведения, пользовательские параметры
- списки воспроизведения метафайлов, пользовательские параметры
- Списки воспроизведения метафайлов Windows Media, пользовательские команды
- списки воспроизведения, пользовательские команды
- списки воспроизведения метафайлов, пользовательские команды
- Списки воспроизведения метафайлов Windows Media, параметры
- списки воспроизведения, параметры
- списки воспроизведения метафайлов, параметры
- пользовательские параметры
- пользовательские команды
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888563"
---
# <a name="using-custom-parameters-and-commands"></a>Использование пользовательских параметров и команд

Можно создать пользовательские параметры для передачи дополнительных метаданных в список воспроизведения метафайлов с помощью элемента **param** . Используйте атрибут **Name** элемента **param** , чтобы определить имя настраиваемого параметра. Используйте атрибут **value** , чтобы определить значение для именованного настраиваемого параметра.

Получите метаданные **param** с помощью методов **getItemInfo** объектов **мультимедиа** и **списков воспроизведения** . Пример использования этих методов для получения метаданных см. в описании метода [аттрибутекаунт](playlist-attributecount.md) объекта **списка воспроизведения** .

В следующем примере списка воспроизведения метафайла показано использование элемента **param** для определения пользовательских параметров.


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование списков воспроизведения метафайлов**](using-metafile-playlists.md)
</dt> </dl>

 

 




